Find Crypto
-----------

show_Paths(d, dx.tainted_packages.search_crypto_packages())

Find Methods
------------

show_Paths(d, dx.tainted_packages.search_methods(“.”, “getIntent”, “.”))

Intent Filters
--------------

activites = a.get_activities()  
for activity in activites: 
  filters = a.get_intent_filters('activity', activity)
  for k,v in filters.items(): 
      print(activity, k,v)
