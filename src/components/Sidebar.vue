<script setup></script>

<template>
  <div
    class="min-h-screen flex flex-col font-[Roboto] p-3 border-r border-[#F1F0F0]"
  >
    <div>
      <img alt="Payman Logo" aria-placeholder="Payman logo" />
      <input type="text" placeholder="Search" />
    </div>
    <article class="flex flex-col flex-grow space-y-2 p-2 mt-3">
      <div class="flex items-center space-x-2">
        <img alt="Dashboard" aria-placeholder="Dashboard" />
        <h2>Dashboard</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF]">
        <img alt="Inbox" aria-placeholder="Inbox" />
        <h2>Inbox</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF]">
        <img alt="Todos" aria-placeholder="Todos" />
        <h2>Todo's</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF]">
        <img alt="Bills" aria-placeholder="Bills" />
        <h2>Bills</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF]">
        <img alt="Contacts" aria-placeholder="Contacts" />
        <h2>Contacts</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF]">
        <img alt="Report" aria-placeholder="Report" />
        <h2>Report</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF]">
        <img alt="Customer" aria-placeholder="Customer" />
        <h2>Customer</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF]">
        <img alt="Accounting" aria-placeholder="Accounting" />
        <h2>Accounting</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF]">
        <img alt="Settings" aria-placeholder="Settings" />
        <h2>Settings</h2>
      </div>
    </article>
    <footer class="flex items-center space-x-2 hover:bg-[#EBF8FF]">
      <div>
        <img alt="ProfileImg" aria-placeholder="Profile Image" />
        <div class="flex flex-col">
          <h2>Profile</h2>
          <p>profile@mail.com</p>
        </div>
      </div>
    </footer>
  </div>
</template>
