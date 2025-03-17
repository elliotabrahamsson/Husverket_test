<template>
  <div
    class="min-h-screen flex flex-col font-[Roboto] p-3 border-t border-[#F1F0F0] w-full"
  >
    <div class="flex items-center justify-between">
      <h1 class="m-4">Bills</h1>
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
          class="border border-[#F1F0F0] hover:bg-blue-500 hover:text-white w-min p-1.5 ml-auto rounded"
        >
          <img alt="SettingsIcon" class="w-2 h-2" />
        </button>
      </div>

      <div
        class="grid grid-cols-17 text-xs border-b border-l-[#ECC94B] border-l-2 border-[#F1F0F0] items-center bg-[#FFF7CF]"
      >
        <input type="checkbox" class="form-checkbox" />

        <div class="flex items-center gap-x-2">
          <img alt="ProfileIcon" class="w-6 h-6 rounded-full" />
          <span>3456874</span>
        </div>

        <p class="px-2">23456754234</p>
        <p class="px-2"></p>
        <p class="px-2"><strong>Google</strong> <br />5684236526</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2">New created</p>
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
          <img alt="ProfileIcon" class="w-6 h-6 rounded-full" />
          <span>3456874</span>
        </div>

        <p class="px-2">23456754234</p>
        <p class="px-2"></p>
        <p class="px-2"><strong>Google</strong> <br />5684236526</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2">New created</p>
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
          <img alt="ProfileIcon" class="w-6 h-6 rounded-full" />
          <span>3456874</span>
        </div>

        <p class="px-2">23456754234</p>
        <p class="px-2"></p>
        <p class="px-2"><strong>Google</strong> <br />5684236526</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2">New created</p>
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
        class="grid grid-cols-17 text-xs border-b border-l-[#D76C6C] border-l-2 border-[#F1F0F0] items-center bg-[#F4C8C8]"
      >
        <input type="checkbox" class="form-checkbox" />

        <div class="flex items-center gap-x-2">
          <img alt="ProfileIcon" class="w-6 h-6 rounded-full" />
          <span>3456874</span>
        </div>

        <p class="px-2">23456754234</p>
        <p class="px-2"></p>
        <p class="px-2"><strong>Google</strong> <br />5684236526</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2">New created</p>
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
          <img alt="ProfileIcon" class="w-6 h-6 rounded-full" />
          <span>3456874</span>
        </div>

        <p class="px-2">23456754234</p>
        <p class="px-2"></p>
        <p class="px-2"><strong>Google</strong> <br />5684236526</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2">New created</p>
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
          <img alt="ProfileIcon" class="w-6 h-6 rounded-full" />
          <span>3456874</span>
        </div>

        <p class="px-2">23456754234</p>
        <p class="px-2"></p>
        <p class="px-2"><strong>Google</strong> <br />5684236526</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2">New created</p>
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
        class="grid grid-cols-17 text-xs border-b border-l-[#74B3FF] border-l-2 border-[#F1F0F0] items-center bg-[#A3CBFA]"
      >
        <input type="checkbox" class="form-checkbox" />

        <div class="flex items-center gap-x-2">
          <img alt="ProfileIcon" class="w-6 h-6 rounded-full" />
          <span>3456874</span>
        </div>

        <p class="px-2">23456754234</p>
        <p class="px-2"></p>
        <p class="px-2"><strong>Google</strong> <br />5684236526</p>
        <p class="px-2">2022-03-09</p>
        <p class="px-2">New created</p>
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
    </div>
  </div>
</template>

<script setup></script>
