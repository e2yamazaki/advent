<template>
<header class="text-gray-600 body-font">
  <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
    <a class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0">
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" stroke="currentColor" class="w-10 h-10 text-white p-2 bg-green-500 rounded-full" viewBox="0 0 24 24"><path d="M11.011 2.39l-1.011-.957 1.389-.189.611-1.244.611 1.244 1.389.189-1.011.957.246 1.36-1.235-.651-1.235.651.246-1.36zm-.011 21.61h2v-3h-2v3zm-2.301-9.82c-1.035 0-2.043-.254-2.665-.672 1.966-.945 3.483-2.422 4.033-4.04-.513 0-1.527-.212-1.934-.543 1.766-.977 3.178-2.789 3.867-4.396.689 1.607 2.101 3.419 3.866 4.396-.406.331-1.421.543-1.934.543.55 1.619 2.067 3.095 4.033 4.041-.622.417-1.63.672-2.664.672.361 1.439 2.312 3.508 4.698 4.334-2.168.991-5.083 1.485-7.996 1.485-2.92 0-5.839-.497-8.003-1.485 2.387-.827 4.336-2.895 4.699-4.335zm5.657 2.015l-.379.78-.857.119.624.601-.152.854.765-.409.765.409-.152-.854.625-.601-.859-.119-.38-.78zm-1.333-4.107c0 .349.282.632.631.632s.631-.283.631-.632c0-.349-.282-.631-.631-.631s-.631.282-.631.631zm-.224 2.913c0-.425-.346-.77-.77-.77-.426 0-.77.344-.77.77 0 .425.344.77.77.77.424 0 .77-.345.77-.77zm-1.42-7.605c0 .349.282.632.631.632.348 0 .631-.283.631-.632 0-.348-.283-.631-.631-.631-.349 0-.631.283-.631.631zm0 2.652c0 .348.282.631.631.631.348 0 .631-.283.631-.631 0-.349-.283-.632-.631-.632-.349.001-.631.284-.631.632zm-1.785 2.05l.456.438-.111.621.557-.298.556.298-.111-.621.455-.438-.625-.086-.274-.567-.275.567-.628.086zm-1 5.362c0 .547.443.991.99.991.548 0 .991-.444.991-.991 0-.547-.443-.991-.991-.991-.547 0-.99.444-.99.991z"/></svg>
      <span class="ml-3 text-xl">Jamstack</span>
    </a>
    <nav class="md:ml-auto flex flex-wrap items-center text-base justify-center">
    </nav>
    <a v-if="this.$route.name === 'post-id'" href="/advent/" class="inline-flex items-center bg-gray-100 border-0 py-1 px-3 focus:outline-none hover:bg-gray-200 rounded text-base mt-4 md:mt-0">Back
      <svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 ml-1" viewBox="0 0 24 24">
        <path d="M5 12h14M12 5l7 7-7 7"></path>
      </svg>
    </a>
  </div>
</header>
</template>
