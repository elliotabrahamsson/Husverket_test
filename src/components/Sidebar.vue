<script setup></script>

<template>
  <div
    class="min-h-screen flex flex-col font-[Roboto] p-3 border-r border-[#F1F0F0]"
  >
    <div class="flex items-center space-x-2">
      <img
        alt="Payman Logo"
        src="../assets/Payman_logga.png"
        aria-placeholder="Payman logo"
      />
      <h1>Payman</h1>
    </div>
    <input type="text" placeholder="Search" class="m-2" />
    <article class="flex flex-col flex-grow space-y-2 p-2 mt-3">
      <div class="flex items-center space-x-2 bg-[#EBF8FF] p-2 rounded">
        <img
          alt="Dashboard"
          src="../assets/Dashboard.png"
          aria-placeholder="Dashboard"
          class="w-6"
        />
        <h2>Dashboard</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF] rounded">
        <img
          alt="Inbox"
          src="../assets/inbox_logga.png"
          aria-placeholder="Inbox"
          class="w-6"
        />
        <h2>Inbox</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF] rounded">
        <img
          alt="Todos"
          src="../assets/Todos_logga.png"
          aria-placeholder="Todos"
          class="w-6"
        />
        <h2>Todo's</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF] rounded">
        <img
          alt="Bills"
          src="../assets/bills_logga.png"
          aria-placeholder="Bills"
          class="w-6"
        />
        <h2>Bills</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF] rounded">
        <img
          alt="Contacts"
          src="../assets/contacts_logga.png"
          aria-placeholder="Contacts"
          class="w-6"
        />
        <h2>Contacts</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF] rounded">
        <img
          alt="Report"
          src="../assets/report_logga.png"
          aria-placeholder="Report"
          class="w-6"
        />
        <h2>Report</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF] rounded">
        <img
          alt="Customer"
          src="../assets/customer_logga.png"
          aria-placeholder="Customer"
          class="w-6"
        />
        <h2>Customer</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF] rounded">
        <img
          alt="Accounting"
          src="../assets/accounting_logga.png"
          aria-placeholder="Accounting"
          class="w-6"
        />
        <h2>Accounting</h2>
      </div>
      <div class="flex items-center space-x-2 hover:bg-[#EBF8FF] rounded">
        <img
          alt="Settings"
          src="../assets/setting_logga.png"
          aria-placeholder="Settings"
          class="w-6"
        />
        <h2>Settings</h2>
      </div>
    </article>
    <footer class="flex flex-col space-x-2 hover:bg-[#EBF8FF]">
      <div class="flex items-center space-x-2">
        <img
          alt="ProfileImg"
          src="../assets/profile-icon-9.png"
          aria-placeholder="Profile Image"
          class="w-6"
        />
        <div class="">
          <h2>Profile</h2>
          <p>profile@mail.com</p>
        </div>
      </div>
    </footer>
  </div>
</template>
