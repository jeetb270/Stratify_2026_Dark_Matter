QUICKCART — PROJECT DARK MATTER
Simulated dataset pack | STRATIFY 2.0 Business Analytics Bootcamp

WHAT'S IN HERE
  order_log.csv          186,156 orders | 1 Apr 2026 - 31 May 2026 (two complete months)
  store_master.csv       18 dark stores across Pune, Hyderabad and Jaipur
  candidate_sites.csv    15 shortlisted properties
  pincode_density.csv    40 pincodes with population density
  data_dictionary.csv    every column in every file, explained

HOW TO JOIN
  order_log.store_id        -> store_master.store_id
  order_log.delivery_pincode-> pincode_density.pincode
  candidate_sites.site_pincode -> pincode_density.pincode

NOTES BEFORE YOU START
  1. Distance is NOT in the data. You compute it yourself, store to delivery point,
     using the haversine formula (or the flat approximation given in the brief).
  2. There is no "breached" flag either. An order is breached when
     actual_delivery_min > promised_delivery_min (10).
  3. Cost-to-serve is not in the data. Build it from the assumptions table in the
     brief: Rs 22 rider base + Rs 7/km + Rs 8 packaging + Rs 30 per breach,
     plus the store's monthly (rent + fixed cost) divided by the orders that store
     fulfilled that month.
  4. Two complete calendar months are provided so the monthly fixed-cost
     allocation in point 3 works cleanly. Do it per month, not across the whole period.
  5. Delivery coordinates are jittered. They are realistic in aggregate but no single
     point is a real address.
  6. This is simulated data created for the bootcamp. Store locations, rents and
     order volumes are fictional and do not describe any real company.

FILE SIZES
  order_log.csv is about 16 MB. It opens fine in Excel, Google Sheets and pandas.
  If Sheets is slow, work in Python or filter to one city first.
