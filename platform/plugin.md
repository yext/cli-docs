---
jsfh: true
sidebarLinks:
- id: plugin
  title: Plugin
title: Plugin
---
<script crossorigin="anonymous" integrity="sha256-CSXorXvZcTkaix6Yvo6HppcZGetbYMGWSFlBw8HfCJo=" src="https://code.jquery.com/jquery-3.4.1.min.js"></script><script src="/js/schema_doc.js"></script><link href="/css/schema_doc.css" rel="stylesheet" type="text/css"/> <div class="container-fluid schema-doc-container"> <div class="row"> <main class="schema-body col"><h1>Plugin</h1> <div class="accordion" id="accordiona_id"> <div class="schema-card"> <div class="schema-card-header" id="headinga_id"> <h2 class="mb-0"><span class="property-name">$id</span><span class="value-type">string</span> <span class="required-property">Required</span></h2> </div> <div aria-labelledby="headinga_id" class="collapse show property-definition-div" data-parent="#accordiona_id" id="a_id"> <div class="schema-card-body"> </div> </div> </div> </div> <div class="accordion" id="accordiona_schema"> <div class="schema-card"> <div class="schema-card-header" id="headinga_schema"> <h2 class="mb-0"><span class="property-name">$schema</span><span class="value-type">const</span> <span class="required-property">Required</span></h2> </div> <div aria-labelledby="headinga_schema" class="collapse show property-definition-div" data-parent="#accordiona_schema" id="a_schema"> <div class="schema-card-body"> <span class="const-value" id="a_schema_const">Specific value: <code>"https://schema.yext.com/config/platform/plugin/v1"</code></span> </div> </div> </div> </div> <div class="accordion" id="accordionglobals"> <div class="schema-card"> <div class="schema-card-header" id="headingglobals"> <h2 class="mb-0"><span class="property-name">globals</span><span class="value-type">object</span></h2> </div> <div aria-labelledby="headingglobals" class="collapse show property-definition-div" data-parent="#accordionglobals" id="globals"> <div class="schema-card-body"> <span class="description"><p>Values to set on the global object for plugin invocations</p> </span> </div> </div> </div> </div> <div class="accordion" id="accordionmemoryLimitMB"> <div class="schema-card"> <div class="schema-card-header" id="headingmemoryLimitMB"> <h2 class="mb-0"><span class="property-name">memoryLimitMB</span><span class="value-type">number</span></h2> </div> <div aria-labelledby="headingmemoryLimitMB" class="collapse show property-definition-div" data-parent="#accordionmemoryLimitMB" id="memoryLimitMB"> <div class="schema-card-body"> <span class="description"><p>The memory limit for the plugin instance, in megabytes</p> </span> <p><span class="badge badge-light restriction numeric-restriction" id="memoryLimitMB_number">Value must be greater or equal to <code>1</code> and lesser or equal to <code>1000</code></span></p> </div> </div> </div> </div> <div class="accordion" id="accordionconcurrency"> <div class="schema-card"> <div class="schema-card-header" id="headingconcurrency"> <h2 class="mb-0"><span class="property-name">concurrency</span><span class="value-type">number</span></h2> </div> <div aria-labelledby="headingconcurrency" class="collapse show property-definition-div" data-parent="#accordionconcurrency" id="concurrency"> <div class="schema-card-body"> <span class="description"><p>A hint to suggest the number of worker instances to create</p> </span> <p><span class="badge badge-light restriction numeric-restriction" id="concurrency_number">Value must be greater or equal to <code>1</code> and lesser or equal to <code>50</code></span></p> </div> </div> </div> </div> </main> </div> </div> 