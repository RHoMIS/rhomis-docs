.. _processing_data:

Managing Data
=============================

Once data has been collected, you will
need to verify a few things before you
access your final results. 

In localisation, you tried to identify units, 
crops, and livestock which are likely to appear
in the survey. It is impossible to anticipate
all potential values which might come up in the 
survey. Enumerators are given the option to input
unexpected values using "free-text-entry" fields.
We do not want this data to be lost, and we give 
project managers the opportunity to verify new values.


.. note::

    Unit extraction, price calculations, and data 
    processing take time. Wait for each stage to 
    finish. The results will load automatically

.. youtube:: LF95SrwI62M
    :width: 100%

|



1. Verifying Units
#######################################

The main units which need to be converted are summarised 
below with examples:

.. list-table:: 
   :widths: 25 50 25 25
   :header-rows: 1

   * - Unit type 
     - Description
     - Example Survey Value 
     - Example Conversion 

   * - bees_honey_production_units 
     - The conversion factor should be used to convert to kilograms/litres.
     - buckets_12_litre 
     - 12 
  
   * - country
     - The conversion factor should be used to convert country names to `two-letter ISO country codes <https://www.iban.com/country-codes>`_.  
     - uganda 
     - UG 

   * - crop_name 
     - The name of crops entered in the survey. Often enumerators may specify "other" crops in a free-text-entry field. Sometimes these crops can be mispelt, or in a language other than English. Here we correct mispellings and translations into standard forms (**all lower case**)  
     - maze 
     - maize 

   * - crop_sold_price_quantityunits
     - The price units for crops which were sold. Please note that only one unit will be converted into a string, "total_income_per_year" will be converted to "total_income_per_year" as this is treated as a special case in the analysis scripts.
     - price_per_50kg_sack
     - 0.02 

   * - crop_yield_units
     - The unit of crops which have been collected. This needs to be converted to kilograms
     - cart_250kg
     - 250

     
   * - eggs_sold_price_timeunits
     - The amount of money made per unit time for selling eggs. This needs to be converted into an income per year
     - income for 3 months
     - 4

   * - eggs_units 
     - The number of eggs collected per year
     - pieces/day
     - 365
     
   * - fertiliser_units 
     - The amount of fertiliser in kg
     - sacks_25kg
     - 25
     
   * - livestock_name 
     -
     -
     -
     
   * - milk_sold_price_timeunits 
     - The names of livestock entered in the survey. As with crop names, enumerators can also enter extra livestock names which are in a different language or mispelt. This conversion is used to standardise livestock names entered in the survey
     - month
     - month
   
   * - 
     - 
     - 0.3_litres
     - 0.3
     
   * - milk_units 
     - The amount of milk  collected in litres per year. There are a number of exceptions which must be kept as text strings, and are dealt with in the analysis scripts (e.g. "per animal per day" and "l/animal/day"
     - l/day
     - 365
     
   * - unitland 
     - The amount of land in hectares
     - acres
     - 0.4




2. Checking Prices, Calories, and Other Units
#######################################################

There are certain conversion factors 
that we can only identify after making 
some initial calculations (see stage above).

In this step 


.. list-table:: 
   :widths: 25 50 25 25
   :header-rows: 1

   * - Unit type 
     - Description
     - Example Survey Value 
     - Example Conversion 

   * - milk_calories 
     - Calories per litre for milk from each type of livestock identified in the survey
     - cattle 
     - 597 

   * - meat_calories 
     - Calories per kilogram of meat from different livestock
     -  cattle 
     -  2197

   * - crop_calories 
     - Calories per kg of crop for different crops
     -  maize
     -  3650

   * - eggs_calories 
     - Calories per kg of egg from different livestock
     - chicken
     - 1550

   * - honey_calories 
     - Calories per litre of honey
     - bees
     - 3040

   * - mean_milk_price_per_litre 
     - Average price of milk for the whole survey (in lcu/litre) for different types of livestock
     - cattle
     - 1.50

   * - mean_meat_price_per_kg 
     - Average price of meat for the whole survey (in lcu/kg) for different types of livestock
     - pigs
     - 8

   * - mean_livestock_price_per_animal 
     - Average price of whole livestock for the whole survey (in lcu/head) for different types of livestock
     - sheep
     - 250

   * - mean_eggs_price_per_kg 
     - Average price of eggs for the whole survey (in lcu/kg) for different types of livestock
     - otherpoultry
     - 4

   * - mean_crop_price_per_lcu_per_kg 
     - Average price of crops for the whole survey (in lcu/kg) for different types of crop
     - maize
     - 1.20

   * - mean_bees_honey_price_per_kg 
     - Average price of honey for the whole survey (lcu/litre)
     - bees
     - 4.50

   * - livestock_count_to_tlu 
     - Conversion of different types of livestock to Tropical Livestock Units (TLU).
     - cattle
     - 0.7

   * - livestock_weight_to_kg 
     - Conversion of different types of livestock to average yield of meat when butchered.
     - oxen
     - 250 


.. note::
    Staple crop is slightly
    different to the other 
    conversion tables. You
    only need to provide one 
    value.

    It is important to think 
    about what is the "staple crop"
    for respondents in your survey,
    as this will be used to estimate
    the potential calories that a household
    could purchase with their income.





3. Accessing Results
#######################################

Once units and prices have been verified. It should be
possible to access your final results. If you collect
more data, you will need to check any new units and 
prices again. 