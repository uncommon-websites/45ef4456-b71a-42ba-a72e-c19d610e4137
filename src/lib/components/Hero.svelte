<script>
  let activeTab = 'Intelligent Routing';
  const tabs = ['Intelligent Routing', 'Multi-Bank Access', 'Fraud Prevention', 'Cascading', '3DS Management', 'BIN Mapping', 'Retry Logic', 'Settlement', 'Analytics', 'Compliance'];
</script>

<section class="pt-32 pb-20 px-6 max-w-7xl mx-auto">
  <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 mb-16">
    <div>
      <h1 class="text-5xl md:text-6xl font-medium tracking-tight text-black leading-[1.1] mb-8">
        Higher approval rates<br /> through intelligent orchestration
      </h1>
    </div>
    <div class="flex flex-col justify-end items-start lg:pl-12">
      <p class="text-xl text-gray-600 mb-6 max-w-md leading-relaxed">
        Connect to 150+ banks across 100+ countries. Optimize every transaction with ML-driven routing and fraud prevention.
      </p>
      <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
        Book Payment Audit
        <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
      </a>
    </div>
  </div>

  <!-- Interactive Visual Section -->
  <div class="rounded-3xl overflow-hidden bg-gray-50 border border-gray-200 shadow-sm">
    <!-- Tabs -->
    <div class="flex overflow-x-auto scrollbar-hide border-b border-gray-200 bg-white/50 backdrop-blur-sm">
      {#each tabs as tab}
        <button 
          class="px-5 py-4 text-sm font-medium whitespace-nowrap transition-colors relative {activeTab === tab ? 'text-black' : 'text-gray-500 hover:text-gray-800'}"
          on:click={() => activeTab = tab}
        >
          {tab}
          {#if activeTab === tab}
            <div class="absolute bottom-0 left-0 right-0 h-0.5 bg-black"></div>
          {/if}
        </button>
      {/each}
    </div>

    <!-- Content Area -->
    <div class="relative h-[500px] bg-gradient-to-br from-gray-900 via-gray-800 to-gray-900 overflow-hidden group">
      <!-- Background pattern -->
      <div class="absolute inset-0 opacity-10" style="background-image: radial-gradient(circle at 2px 2px, white 1px, transparent 0); background-size: 40px 40px;"></div>
      
      <!-- Floating UI Card - Payment Routing Dashboard -->
      <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[420px] bg-white rounded-2xl p-5 shadow-2xl">
        <div class="flex justify-between items-center mb-5 pb-3 border-b border-gray-100">
          <span class="text-sm font-semibold text-black">Transaction Routing</span>
          <span class="text-xs text-gray-500">Real-time</span>
        </div>
        
        <!-- Routing Attempt 1 - Failed -->
        <div class="flex items-start gap-3 mb-4 p-3 bg-red-50 rounded-lg border border-red-100">
          <div class="w-8 h-8 rounded-full bg-red-500 flex items-center justify-center text-white shrink-0 text-xs font-bold">
            ✕
          </div>
          <div class="flex-1 min-w-0">
            <div class="flex justify-between items-baseline mb-1">
              <h3 class="text-sm font-semibold text-gray-900">Bank A</h3>
              <span class="text-xs font-medium text-red-600">Declined</span>
            </div>
            <p class="text-xs text-gray-500">Insufficient funds • 43ms</p>
          </div>
        </div>

        <!-- Routing Attempt 2 - Failed -->
        <div class="flex items-start gap-3 mb-4 p-3 bg-orange-50 rounded-lg border border-orange-100">
          <div class="w-8 h-8 rounded-full bg-orange-500 flex items-center justify-center text-white shrink-0 text-xs font-bold">
            ✕
          </div>
          <div class="flex-1 min-w-0">
            <div class="flex justify-between items-baseline mb-1">
              <h3 class="text-sm font-semibold text-gray-900">Bank B</h3>
              <span class="text-xs font-medium text-orange-600">Declined</span>
            </div>
            <p class="text-xs text-gray-500">Risk threshold • 38ms</p>
          </div>
        </div>

        <!-- Routing Attempt 3 - Success -->
        <div class="flex items-start gap-3 p-3 bg-green-50 rounded-lg border border-green-200">
          <div class="w-8 h-8 rounded-full bg-green-500 flex items-center justify-center text-white shrink-0 text-xs font-bold">
            ✓
          </div>
          <div class="flex-1 min-w-0">
            <div class="flex justify-between items-baseline mb-1">
              <h3 class="text-sm font-semibold text-gray-900">Bank C</h3>
              <span class="text-xs font-medium text-green-600">Approved</span>
            </div>
            <p class="text-xs text-gray-500">€249.00 • 3DS passed • 127ms</p>
          </div>
        </div>

        <div class="mt-4 pt-3 border-t border-gray-100 flex justify-between items-center">
          <span class="text-xs text-gray-500">Total routing time</span>
          <span class="text-sm font-semibold text-black">208ms</span>
        </div>
      </div>
    </div>

    <!-- Code Block -->
    <div class="bg-gray-50 p-6 border-t border-gray-200 overflow-x-auto">
      <pre class="font-mono text-xs leading-relaxed text-gray-600">
<span class="text-gray-400 select-none">1</span>  <span class="text-gray-400"># Process payment with intelligent routing across multiple banks</span>
<span class="text-gray-400 select-none">2</span>
<span class="text-gray-400 select-none">3</span>  <span class="text-purple-600">curl</span> <span class="text-blue-600">-X POST</span> <span class="text-green-600">'https://api.crossbill.com/v1/payments'</span> \
<span class="text-gray-400 select-none">4</span>    <span class="text-blue-600">-H</span> <span class="text-green-600">'Authorization: Bearer YOUR_API_KEY'</span> \
<span class="text-gray-400 select-none">5</span>    <span class="text-blue-600">-H</span> <span class="text-green-600">'Content-Type: application/json'</span> \
<span class="text-gray-400 select-none">6</span>    <span class="text-blue-600">-d</span> '&#123;
<span class="text-gray-400 select-none">7</span>      <span class="text-blue-800">"amount"</span>: <span class="text-orange-600">24900</span>,
<span class="text-gray-400 select-none">8</span>      <span class="text-blue-800">"currency"</span>: <span class="text-green-600">"EUR"</span>,
<span class="text-gray-400 select-none">9</span>      <span class="text-blue-800">"routing_strategy"</span>: <span class="text-green-600">"optimize_approval"</span>,
<span class="text-gray-400 select-none">10</span>     <span class="text-blue-800">"cascade_enabled"</span>: <span class="text-purple-600">true</span>,
<span class="text-gray-400 select-none">11</span>     <span class="text-blue-800">"fraud_check"</span>: <span class="text-green-600">"ml_enhanced"</span>,
<span class="text-gray-400 select-none">12</span>     <span class="text-blue-800">"card"</span>: &#123; <span class="text-blue-800">"token"</span>: <span class="text-green-600">"tok_visa_4242"</span> &#125;</pre>
    </div>
  </div>
</section>
