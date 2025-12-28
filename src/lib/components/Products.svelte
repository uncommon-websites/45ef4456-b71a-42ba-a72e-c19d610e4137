<script>
  // No script needed
</script>

<div class="space-y-32 pb-32">
  <!-- Orchestration Platform Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Orchestration Platform</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">Intelligent payment routing.</strong> One API to access 150+ banks and processors. Optimize every transaction with ML-driven routing, cascading logic, and real-time analytics.
      </p>
      <div class="flex flex-col gap-2">
        <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Learn more 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="#" class="text-sm text-gray-400 hover:text-black transition-colors">View docs</a>
      </div>
    </div>
    <div class="bg-gray-50 rounded-3xl p-12 flex items-center justify-center min-h-[400px]">
      <!-- Orchestration Visualization -->
      <div class="relative w-full max-w-md">
        <div class="flex justify-between items-center">
          <!-- Central Hub -->
          <div class="w-16 h-16 bg-black rounded-lg flex items-center justify-center relative z-10">
            <svg width="32" height="32" viewBox="0 0 24 24" fill="white"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/></svg>
          </div>
          
          <!-- Bank Endpoints -->
          <div class="flex flex-col gap-3">
            {#each ['Axiom', 'Citizens', 'TSYS', 'Fiserv', 'Dart', 'eMerchant', 'Global'] as item, i}
              <div class="flex items-center gap-4">
                <div class="w-24 h-[1px] bg-gradient-to-r from-black/20 to-transparent transform rotate-180 origin-left"></div>
                <div class="flex items-center gap-2">
                  <div class="w-3 h-3 rounded-full" style="background-color: hsl({i * 50}, 70%, 50%)"></div>
                  <span class="text-xs font-medium text-gray-600">{item}</span>
                </div>
              </div>
            {/each}
          </div>
        </div>
        <!-- Connecting lines (simplified) -->
        <svg class="absolute inset-0 w-full h-full pointer-events-none" style="z-index: 0;">
          <defs>
            <linearGradient id="lineGradient" x1="0%" y1="0%" x2="100%" y2="0%">
              <stop offset="0%" stop-color="#000" stop-opacity="0.1" />
              <stop offset="100%" stop-color="#000" stop-opacity="0" />
            </linearGradient>
          </defs>
          <!-- Curved lines would go here, but using straight CSS lines above for simplicity -->
        </svg>
      </div>
    </div>
  </section>

  <!-- Global Banking Access Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Global Banking Access</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">150+ banks, 100+ countries.</strong> CrossBill handles banking relationships, compliance, and settlement flows—so you can expand globally without the operational overhead.
      </p>
      <div class="flex flex-col gap-2">
        <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Learn more 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="#" class="text-sm text-gray-400 hover:text-black transition-colors">View coverage map</a>
      </div>
    </div>
    <div class="bg-gradient-to-br from-blue-50 to-purple-50 rounded-3xl overflow-hidden min-h-[400px] relative flex items-center justify-center p-8">
      <!-- World Map Simplified -->
      <div class="relative w-full h-full flex items-center justify-center">
        <div class="absolute inset-0 opacity-20" style="background-image: radial-gradient(circle, #000 1px, transparent 1px); background-size: 20px 20px;"></div>
        <div class="text-center z-10">
          <div class="text-6xl font-bold text-black mb-4">150+</div>
          <div class="text-lg text-gray-600 mb-6">Banking Partners</div>
          <div class="flex gap-8 justify-center text-sm">
            <div><span class="font-bold text-2xl text-black">100+</span><br/><span class="text-gray-500">Countries</span></div>
            <div><span class="font-bold text-2xl text-black">400+</span><br/><span class="text-gray-500">Integrations</span></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Fraud Prevention Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Fraud Prevention</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">ML-driven risk management.</strong> Proprietary machine learning models combined with rule-based systems and scheme alerts to reduce fraud while maintaining high approval rates.
      </p>
      <div class="flex flex-col gap-2">
        <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Learn more 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="#" class="text-sm text-gray-400 hover:text-black transition-colors">View risk controls</a>
      </div>
    </div>
    <div class="bg-gradient-to-br from-gray-900 to-gray-800 rounded-3xl p-12 flex items-center justify-center min-h-[400px]">
      <!-- Dashboard Mockup -->
      <div class="relative w-full bg-white rounded-2xl shadow-2xl overflow-hidden">
        <!-- Screen Content -->
        <div class="p-6">
          <div class="flex justify-between items-center mb-6 pb-4 border-b border-gray-100">
            <span class="text-sm font-semibold">Risk Dashboard</span>
            <div class="flex gap-2">
              <div class="w-2 h-2 rounded-full bg-green-500"></div>
              <div class="w-2 h-2 rounded-full bg-yellow-500"></div>
              <div class="w-2 h-2 rounded-full bg-red-500"></div>
            </div>
          </div>
          <div class="space-y-4">
             <div class="flex items-center justify-between p-3 bg-green-50 rounded-lg border border-green-200">
               <div class="flex items-center gap-3">
                 <div class="w-8 h-8 rounded-full bg-green-500 flex items-center justify-center text-white text-xs font-bold">✓</div>
                 <div>
                   <div class="text-xs font-semibold text-gray-900">Low Risk</div>
                   <div class="text-[10px] text-gray-500">Score: 12/100</div>
                 </div>
               </div>
               <div class="text-xs font-bold text-green-600">87%</div>
             </div>
             <div class="flex items-center justify-between p-3 bg-yellow-50 rounded-lg border border-yellow-200">
               <div class="flex items-center gap-3">
                 <div class="w-8 h-8 rounded-full bg-yellow-500 flex items-center justify-center text-white text-xs font-bold">!</div>
                 <div>
                   <div class="text-xs font-semibold text-gray-900">Medium Risk</div>
                   <div class="text-[10px] text-gray-500">Score: 45/100</div>
                 </div>
               </div>
               <div class="text-xs font-bold text-yellow-600">11%</div>
             </div>
             <div class="flex items-center justify-between p-3 bg-red-50 rounded-lg border border-red-200">
               <div class="flex items-center gap-3">
                 <div class="w-8 h-8 rounded-full bg-red-500 flex items-center justify-center text-white text-xs font-bold">✕</div>
                 <div>
                   <div class="text-xs font-semibold text-gray-900">High Risk</div>
                   <div class="text-[10px] text-gray-500">Score: 89/100</div>
                 </div>
               </div>
               <div class="text-xs font-bold text-red-600">2%</div>
             </div>
          </div>
          <div class="mt-4 pt-4 border-t border-gray-100">
            <div class="text-[10px] text-gray-400 mb-2">Chargeback Ratio</div>
            <div class="text-lg font-bold text-black">0.18%</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</div>
