
# Data Wrangle OpenStreetMap Project

MAP AREA: Toronto - Canada

http://www.openstreetmap.org/export#map=11/43.7188/-79.3762

https://www.openstreetmap.org/relation/324211

I lived in Toronto, CANADA. I am intrested in find more about the places and streets.  I would like to analyse and check its need any corrections or improvements.

1. When I audit the data for the Street and found that some of the street name abbreviation are not what we expected. I able to improve or update the Stree name abbreviation to the expected name.
  
   * 'Rd.' -> Road
   * 'st'  -> Street
   * 'Ter' -> Terrace


2. When I audit the Postal Code, some of them are missing a space as follows 'L1W3R2'. 
   * The right format is :'L1W 3R2'. 

3. When I audit the Phone numbers. some of them are notin the right format. I able to corrected to the right format as follows.
   * '+1 905 990 9220' -> '+1-905-990-9220'
   * Also seen abnormal format as follows,
       * 'unknown''(416) 536-SODA',
                 '+1 905 -90-4110',
                 '1 905 891 326',
                 '439-0000'

 Exploring the Data
1. Number of Nodes.
In [15]:

cur.execute("SELECT COUNT(*) from nodes;")
print 'There are {} nodes.'.format(cur.fetchall()[0][0])
There are 341835 nodes.
