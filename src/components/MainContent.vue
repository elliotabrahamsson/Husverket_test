<script setup>
import { onMounted } from "vue";

onMounted(() => {
  const openModalBtn = document.querySelectorAll("[data-modal-target]");
  const closeModalBtn = document.querySelectorAll("[data-close-button]");
  const overlay = document.getElementById("overlay");

  openModalBtn.forEach((button) => {
    button.addEventListener("click", () => {
      const modal = document.querySelector(button.dataset.modalTarget);
      toggleModal(modal);
    });
  });

  closeModalBtn.forEach((button) => {
    button.addEventListener("click", () => {
      const modal = button.closest(".modal");
      hideModal(modal);
    });
  });

  function toggleModal(modal) {
    if (!modal) return;
    const isActive = modal.classList.contains("active");

    if (isActive) {
      hideModal(modal);
    } else {
      showModal(modal);
    }
  }

  function showModal(modal) {
    if (!modal) return;
    modal.classList.add("active");
    overlay.classList.add("active");
  }

  function hideModal(modal) {
    if (!modal) return;
    modal.classList.remove("active");
    overlay.classList.remove("active");
  }

  overlay.addEventListener("click", () => {
    const modals = document.querySelectorAll(".modal.active");
    modals.forEach((modal) => hideModal(modal));
  });
});
</script>

<template>
  <div
    class="min-h-screen flex flex-col font-[Roboto] p-3 border-t border-[#F1F0F0] w-full"
  >
    <div class="flex items-center justify-between">
      <h1 class="m-4 ml-10">Bills</h1>
      <ul class="flex justify-end space-x-6 p-2">
        <li class="flex items-center space-x-2">
          <button
            class="flex items-center space-x-1.5 border border-[#F1F0F0] text-black hover:bg-blue-500 hover:text-white p-1.5 rounded"
          >
            <span>All</span>
          </button>
          <button
            class="flex items-center space-x-1.5 border border-[#F1F0F0] text-black hover:bg-blue-500 hover:text-white p-1.5 rounded"
          >
            <div class="w-1 h-4 bg-[#EBC641] rounded-full"></div>
            <span>New</span>
          </button>
          <button
            class="flex items-center space-x-1.5 border border-[#F1F0F0] text-black hover:bg-blue-500 hover:text-white p-1.5 rounded"
          >
            <div class="w-1 h-4 bg-[#F55E5E] rounded-full"></div>
            <span>Unpaid</span>
          </button>
          <button
            class="flex items-center space-x-1.5 border border-[#F1F0F0] text-black hover:bg-blue-500 hover:text-white p-1.5 rounded"
          >
            <div class="w-1 h-4 bg-[#40B872] rounded-full"></div>
            <span>Paid</span>
          </button>
          <button
            class="flex items-center space-x-1.5 border border-[#F1F0F0] text-black hover:bg-blue-500 hover:text-white p-1.5 rounded"
          >
            <div class="w-1 h-4 bg-[#9C76E9] rounded-full"></div>
            <span>Has reminder</span>
          </button>
          <button
            class="flex items-center space-x-1.5 border border-[#F1F0F0] text-black hover:bg-blue-500 hover:text-white p-1.5 rounded"
          >
            <span>Invistagtion</span>
          </button>
          <button
            class="flex items-center space-x-1.5 border border-[#F1F0F0] text-black hover:bg-blue-500 hover:text-white p-1.5 rounded"
          >
            <span>Inkasso</span>
          </button>
          <button
            class="flex items-center space-x-1.5 border border-[#F1F0F0] text-black hover:bg-blue-500 hover:text-white p-1.5 rounded"
          >
            <span>Kronofogden</span>
          </button>
        </li>
      </ul>
    </div>
    <div class="w-fit-content">
      <div
        class="grid grid-cols-17 text-xs border-b border-[#F1F0F0] font-bold items-center"
      >
        <input type="checkbox" class="form-checkbox" />
        <p class="px-2">FACR NO</p>
        <p class="px-2">OCR</p>
        <p class="px-2">TYPE OF</p>
        <p class="px-2">NAME & NUMBER</p>
        <p class="px-2">FACT DATE</p>
        <p class="px-2">CATEGORY</p>
        <p class="px-2">DELIVERY DATE</p>
        <p class="px-2">TOTAL</p>
        <p class="px-2">BALANCE</p>
        <p class="px-2">VISIBILITY</p>
        <p class="px-2">PRE-DATE</p>
        <p class="px-2">FINAL PAID</p>
        <p class="px-2">CATEGORY</p>
        <p class="px-2">UPTAKEN</p>
        <p class="px-2">COST</p>
        <button
          data-modal-target="#modal"
          class="border border-[#F1F0F0] hover:bg-blue-500 hover:text-white ml-auto w-max p-1 rounded"
        >
          <img
            alt="SettingsIcon"
            src="../assets/settings-icon.png"
            class="w-4 h-4"
          />
        </button>
      </div>

      <div
        class="grid grid-cols-17 text-xs border-b border-l-[#ECC94B] border-l-2 border-[#F1F0F0] items-center bg-[#FFF7CF]"
      >
        <input type="checkbox" class="form-checkbox" />

        <div class="flex items-center gap-x-2">
          <img
            alt="ProfileIcon"
            src="../assets/profile-icon-9.png"
            class="w-6 h-6 rounded-full"
          />
          <span>3456874</span>
        </div>

        <p class="px-2">23456754234</p>
        <p class="px-2"></p>
        <p class="px-2"><strong>Google</strong> <br />5684236526</p>
        <p class="px-2">2022-03-09</p>
        <p
          data-modal-target="#modalData"
          class="px-2 bg-[#EDE6C1] rounded-3xl cursor-pointer w-fit font-bold"
        >
          New created
        </p>
        <p class="px-2">-</p>
        <p class="px-2">543,000</p>
        <p class="px-2">543,000</p>
        <p class="px-2">Opened</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2">543,000</p>
        <p class="px-2">A21</p>
        <p class="px-2">2345</p>
        <p class="px-2"></p>
      </div>
      <div
        class="grid grid-cols-17 text-xs border-b border-l-[#40B872] border-l-2 border-[#F1F0F0] items-center bg-[#D6EDCB]"
      >
        <input type="checkbox" class="form-checkbox" />

        <div class="flex items-center gap-x-2">
          <img
            alt="ProfileIcon"
            src="../assets/profile-icon-9.png"
            class="w-6 h-6 rounded-full"
          />
          <span>3456874</span>
        </div>

        <p class="px-2">23456754234</p>
        <p class="px-2 text-center bg-[#C3E3B8] rounded-3xl w-fit">F</p>
        <p class="px-2"><strong>Google</strong> <br />5684236526</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2 bg-[#C3E3B8] rounded-3xl w-fit font-bold">New created</p>
        <p class="px-2">-</p>
        <p class="px-2">543,000</p>
        <p class="px-2">543,000</p>
        <p class="px-2">Opened</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2">543,000</p>
        <p class="px-2">A21</p>
        <p class="px-2">2345</p>
        <p class="px-2"></p>
      </div>
      <div
        class="grid grid-cols-17 text-xs border-b border-l-[#FFFFF] border-l-2 border-[#F1F0F0] items-center bg-[#FFFFF]"
      >
        <input type="checkbox" class="form-checkbox" />

        <div class="flex items-center gap-x-2">
          <img
            alt="ProfileIcon"
            src="../assets/profile-icon-9.png"
            class="w-6 h-6 rounded-full"
          />
          <span>3456874</span>
        </div>

        <p class="px-2">23456754234</p>
        <p class="px-2 text-center bg-[#F0F0F0] rounded-3xl w-fit">F</p>
        <p class="px-2"><strong>Google</strong> <br />5684236526</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2 bg-[#F0F0F0] rounded-3xl w-fit font-bold">New created</p>
        <p class="px-2">-</p>
        <p class="px-2">543,000</p>
        <p class="px-2">543,000</p>
        <p class="px-2">Not opened</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2">543,000</p>
        <p class="px-2">A21</p>
        <p class="px-2">2345</p>
        <p class="px-2"></p>
      </div>
      <div
        class="grid grid-cols-17 text-xs border-b border-l-[#D76C6C] border-l-2 border-[#F1F0F0] items-center bg-[#F4C8C8]"
      >
        <input type="checkbox" class="form-checkbox" />

        <div class="flex items-center gap-x-2">
          <img
            alt="ProfileIcon"
            src="../assets/profile-icon-9.png"
            class="w-6 h-6 rounded-full"
          />
          <span>3456874</span>
        </div>

        <p class="px-2">23456754234</p>
        <p class="px-2 text-center bg-[#EAB0B0] rounded-3xl w-fit">F</p>
        <p class="px-2"><strong>Google</strong> <br />5684236526</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2 bg-[#EAB0B0] rounded-3xl w-fit font-bold">New created</p>
        <p class="px-2">-</p>
        <p class="px-2">543,000</p>
        <p class="px-2">543,000</p>
        <p class="px-2">Opened</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2">543,000</p>
        <p class="px-2">A21</p>
        <p class="px-2">2345</p>
        <p class="px-2"></p>
      </div>
      <div
        class="grid grid-cols-17 text-xs border-b border-l-[#ECC94B] border-l-2 border-[#F1F0F0] items-center bg-[#FFF7CF]"
      >
        <input type="checkbox" class="form-checkbox" />

        <div class="flex items-center gap-x-2">
          <img
            alt="ProfileIcon"
            src="../assets/profile-icon-9.png"
            class="w-6 h-6 rounded-full"
          />
          <span>3456874</span>
        </div>

        <p class="px-2">23456754234</p>
        <p class="px-2 text-center bg-[#EDE6C1] rounded-3xl w-fit">F</p>
        <p class="px-2"><strong>Google</strong> <br />5684236526</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2 bg-[#EDE6C1] rounded-3xl w-fit font-bold">New created</p>
        <p class="px-2">-</p>
        <p class="px-2">543,000</p>
        <p class="px-2">543,000</p>
        <p class="px-2">Opened</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2">543,000</p>
        <p class="px-2">A21</p>
        <p class="px-2">2345</p>
        <p class="px-2"></p>
      </div>
      <div
        class="grid grid-cols-17 text-xs border-b border-l-[#4B81E9] border-l-2 border-[#F1F0F0] items-center bg-[#AEB5F4]"
      >
        <input type="checkbox" class="form-checkbox" />

        <div class="flex items-center gap-x-2">
          <img
            alt="ProfileIcon"
            src="../assets/profile-icon-9.png"
            class="w-6 h-6 rounded-full"
          />
          <span>3456874</span>
        </div>

        <p class="px-2">23456754234</p>
        <p class="px-2 text-center bg-[#A1A7E2] rounded-3xl w-fit">F</p>
        <p class="px-2"><strong>Google</strong> <br />5684236526</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2 bg-[#A1A7E2] rounded-3xl w-fit font-bold">Collection</p>
        <p class="px-2">-</p>
        <p class="px-2">543,000</p>
        <p class="px-2">543,000</p>
        <p class="px-2">Not opened</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2">543,000</p>
        <p class="px-2">A21</p>
        <p class="px-2">2345</p>
        <p class="px-2"></p>
      </div>
      <div
        class="grid grid-cols-17 text-xs border-b border-l-[#74B3FF] border-l-2 border-[#F1F0F0] items-center bg-[#A3CBFA]"
      >
        <input type="checkbox" class="form-checkbox" />

        <div class="flex items-center gap-x-2">
          <img
            alt="ProfileIcon"
            src="../assets/profile-icon-9.png"
            class="w-6 h-6 rounded-full"
          />
          <span>3456874</span>
        </div>

        <p class="px-2">23456754234</p>
        <p class="px-2 text-center bg-[#98BDE9] rounded-3xl w-fit">F</p>
        <p class="px-2"><strong>Google</strong> <br />5684236526</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2 bg-[#98BDE9] rounded-3xl font-bold w-fit">Collection</p>
        <p class="px-2">-</p>
        <p class="px-2">543,000</p>
        <p class="px-2">543,000</p>
        <p class="px-2">Not opened</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2">543,000</p>
        <p class="px-2">A21</p>
        <p class="px-2">2345</p>
        <p class="px-2"></p>
      </div>
    </div>

    <div id="overlay" class="w-max h-auto">
      <div
        class="border shadow border-[#F1F0F0] bg-[#FFFFFF] flex-col hidden p-3 rounded z-10 absolute top-[18%] left-[86%]"
        id="modal"
      >
        <div id="modalHeader">
          <h2>Customize view</h2>
        </div>
        <div id="modalContent" class="flex flex-col">
          <input type="text" placeholder="Search" class="border p-1 rounded" />

          <label class="flex items-center space-x-2">
            <input type="checkbox" class="form-checkbox" /> <span>All</span>
          </label>

          <label class="flex items-center space-x-2">
            <input type="checkbox" class="form-checkbox" />
            <span>Visibility</span>
          </label>

          <label class="flex items-center space-x-2">
            <input type="checkbox" class="form-checkbox" />
            <span>Category</span>
          </label>

          <label class="flex items-center space-x-2">
            <input type="checkbox" class="form-checkbox" />
            <span>Final Paid</span>
          </label>

          <label class="flex items-center space-x-2">
            <input type="checkbox" class="form-checkbox" />
            <span>Category</span>
          </label>

          <label class="flex items-center space-x-2">
            <input type="checkbox" class="form-checkbox" />
            <span>Fact Date</span>
          </label>
        </div>
        <div
          class="border-t border-[#F1F0F0] flex items-center justify-end space-x-2 p-2"
        >
          <button class="border border-[#F1F0F0] p-1.5 rounded shadow">
            Cancel
          </button>
          <button class="border border-[#F1F0F0] p-1.5 rounded shadow">
            Apply
          </button>
        </div>
      </div>
    </div>

    <div
      id="modalData"
      class="hidden border shadow border-[#F1F0F0] rounded w-[26rem] z-10 absolute top-[31%] left-[54%] transform -translate-x-1/2 -translate-y-1/2 bg-white"
    >
      <div id="modalContent">
        <p class="text-xs font-bold bg-[#F7FAFC] p-2">REMINDER HISTORY</p>
        <div class="flex flex-col space-x-2 border-t border-[#F1F0F0] p-2">
          <div class="flex items-center justify-between space-x-2">
            <h1>Change Ticket</h1>
            <p class="ml-auto bg-[#98BDE9] text-xs px-2 rounded-2xl w-max">
              Unpaid due
            </p>
          </div>
          <p class="text-xs">22. Jul 2022</p>
        </div>
      </div>
      <div class="flex flex-col space-x-2 border-t border-[#F1F0F0] p-2">
        <div>
          <div class="flex items-center justify-between space-x-2">
            <h1>Send reminder</h1>
          </div>
          <p class="text-xs">22. Jul 2022</p>
        </div>
      </div>
      <div class="flex flex-col space-x-2 border-t border-[#F1F0F0] p-2">
        <div>
          <div class="flex items-center justify-between space-x-2">
            <h1>Change Ticket</h1>
            <p class="ml-auto bg-[#98BDE9] text-xs px-2 rounded-2xl w-max">
              Send reminder
            </p>
          </div>
          <p class="text-xs">22. Jul 2022</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.active {
  display: block;
}
</style>
