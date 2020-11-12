=============================
Spot Classsifer API Docs
=============================


The `Houston.AI classifier <https://houston.ai/api/classify-docs>`_ is an API service that takes text and returns one or more legal problem codes.  


Example
==========

When using entities-nested, the results return the entire hierarchical chain of problem codes where they exist.

.. code-block:: json

   {"build":5,"query-id":"8d27212cb01a470781883942d8bfa020","text":"My landlord is trying to evict me","save-text":1,"cutoff-lower":0,"cutoff-pred":0.51,"cutoff-upper":0.5,"labels":
   [
   {"id":"HO-00-00-00-00","name":"Housing","lower":0.6702660283747915,"pred":0.6968044802596818,"upper":0.7231564346121119,"children":
   [
   {"id":"HO-02-00-00-00","name":"Eviction from a home","lower":0.4510838081510812,"pred":0.8720953624254235,"upper":0.9232572174552537,"children":
   [
   {"id":"HO-02-01-00-00","name":"Eviction from a homeless shelter or group home","lower":0.5927350486282457,"pred":0.8893196920078001,"upper":0.9262311423782457},
   {"id":"HO-02-03-00-00","name":"Eviction from private rental housing (not public or subsidized)","lower":0.6703774769222283,"pred":0.9220504182247975,"upper":0.9376555591075285},
   {"id":"HO-02-04-00-00","name":"Defenses to stop or delay an eviction","lower":0.6619295040045312,"pred":0.9266108162688175,"upper":0.9510858223666679,"children":
   [
   {"id":"HO-02-04-01-00","name":"Notice and Procedural defenses against an eviction","lower":0.7822015239462637,"pred":0.89394459879573,"upper":0.917512465730012},
   {"id":"HO-02-04-03-00","name":"Living conditions (habitability) defenses against an eviction","lower":0.575730354436689,"pred":0.8952891160868177,"upper":0.932663948186689},
   {"id":"HO-02-04-05-00","name":"Title and ownership defenses against an eviction","lower":0.5171006856180037,"pred":0.9049261998315066,"upper":0.9456721141894324},
   {"id":"HO-02-04-06-00","name":"Retaliatory Eviction defenses against an eviction","lower":0.5405569899829392,"pred":0.8496244938488562,"upper":0.8947077754781543}]}]},
   {"id":"HO-06-00-00-00","name":"Renting or leasing a home","lower":0.7056405686109303,"pred":0.9204789073345129,"upper":0.935466769526348,"children":
   [
   {"id":"HO-02-00-00-00","name":"Eviction from a home","lower":0.4510838081510812,"pred":0.8720953624254235,"upper":0.9232572174552537,"children":
   [
   {"id":"HO-02-01-00-00","name":"Eviction from a homeless shelter or group home","lower":0.5927350486282457,"pred":0.8893196920078001,"upper":0.9262311423782457},
   {"id":"HO-02-03-00-00","name":"Eviction from private rental housing (not public or subsidized)","lower":0.6703774769222283,"pred":0.9220504182247975,"upper":0.9376555591075285},
   {"id":"HO-02-04-00-00","name":"Defenses to stop or delay an eviction","lower":0.6619295040045312,"pred":0.9266108162688175,"upper":0.9510858223666679,"children":
   [
   {"id":"HO-02-04-01-00","name":"Notice and Procedural defenses against an eviction","lower":0.7822015239462637,"pred":0.89394459879573,"upper":0.917512465730012},
   {"id":"HO-02-04-03-00","name":"Living conditions (habitability) defenses against an eviction","lower":0.575730354436689,"pred":0.8952891160868177,"upper":0.932663948186689},
   {"id":"HO-02-04-05-00","name":"Title and ownership defenses against an eviction","lower":0.5171006856180037,"pred":0.9049261998315066,"upper":0.9456721141894324},
   {"id":"HO-02-04-06-00","name":"Retaliatory Eviction defenses against an eviction","lower":0.5405569899829392,"pred":0.8496244938488562,"upper":0.8947077754781543}]}]}]}]}]}
   
When using entities-terminal, the results return only the lowest available terms.

.. code-block:: json

   {"build":5,"query-id":"8d27212cb01a470781883942d8bfa020","text":"My landlord is trying to evict me","save-text":1,"cutoff-lower":0,"cutoff-pred":0.51,"cutoff-upper":0.5,"labels":[{"id":"HO-00-00-00-00","name":"Housing","lower":0.6702660283747915,"pred":0.6968044802596818,"upper":0.7231564346121119,"children":
   [{"id":"HO-02-00-00-00","name":"Eviction from a home","lower":0.4510838081510812,"pred":0.8720953624254235,"upper":0.9232572174552537,"children":
   [
   {"id":"HO-02-01-00-00","name":"Eviction from a homeless shelter or group home","lower":0.5927350486282457,"pred":0.8893196920078001,"upper":0.9262311423782457},
   {"id":"HO-02-03-00-00","name":"Eviction from private rental housing (not public or subsidized)","lower":0.6703774769222283,"pred":0.9220504182247975,"upper":0.9376555591075285},
   {"id":"HO-02-04-00-00","name":"Defenses to stop or delay an eviction","lower":0.6619295040045312,"pred":0.9266108162688175,"upper":0.9510858223666679,"children":
   [
   {"id":"HO-02-04-01-00","name":"Notice and Procedural defenses against an eviction","lower":0.7822015239462637,"pred":0.89394459879573,"upper":0.917512465730012},
   {"id":"HO-02-04-03-00","name":"Living conditions (habitability) defenses against an eviction","lower":0.575730354436689,"pred":0.8952891160868177,"upper":0.932663948186689},
   {"id":"HO-02-04-05-00","name":"Title and ownership defenses against an eviction","lower":0.5171006856180037,"pred":0.9049261998315066,"upper":0.9456721141894324},
   {"id":"HO-02-04-06-00","name":"Retaliatory Eviction defenses against an eviction","lower":0.5405569899829392,"pred":0.8496244938488562,"upper":0.8947077754781543}]}]},
   {"id":"HO-06-00-00-00","name":"Renting or leasing a home","lower":0.7056405686109303,"pred":0.9204789073345129,"upper":0.935466769526348,"children":
   [
   {"id":"HO-02-00-00-00","name":"Eviction from a home","lower":0.4510838081510812,"pred":0.8720953624254235,"upper":0.9232572174552537,"children":
   [
   {"id":"HO-02-01-00-00","name":"Eviction from a homeless shelter or group home","lower":0.5927350486282457,"pred":0.8893196920078001,"upper":0.9262311423782457},
   {"id":"HO-02-03-00-00","name":"Eviction from private rental housing (not public or subsidized)","lower":0.6703774769222283,"pred":0.9220504182247975,"upper":0.9376555591075285},
   {"id":"HO-02-04-00-00","name":"Defenses to stop or delay an eviction","lower":0.6619295040045312,"pred":0.9266108162688175,"upper":0.9510858223666679,"children":[
   {"id":"HO-02-04-01-00","name":"Notice and Procedural defenses against an eviction","lower":0.7822015239462637,"pred":0.89394459879573,"upper":0.917512465730012},
   {"id":"HO-02-04-03-00","name":"Living conditions (habitability) defenses against an eviction","lower":0.575730354436689,"pred":0.8952891160868177,"upper":0.932663948186689},
   {"id":"HO-02-04-05-00","name":"Title and ownership defenses against an eviction","lower":0.5171006856180037,"pred":0.9049261998315066,"upper":0.9456721141894324},
   {"id":"HO-02-04-06-00","name":"Retaliatory Eviction defenses against an eviction","lower":0.5405569899829392,"pred":0.8496244938488562,"upper":0.8947077754781543}]}]}]}]}]}   