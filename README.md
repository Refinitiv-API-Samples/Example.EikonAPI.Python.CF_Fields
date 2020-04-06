# Decoding CF_ fields in Eikon

This Jupyter Notebook illustrates how consolidated fields aka CF_ fields are mapped to FIDs on Elektron.
In Eikon real-time data fields whose names start with "CF_" such as CF_LAST, CF_BID etc. do not come directly from Elektron datafeed. Eikon implements a logic that maps CF_ fields to Elektron FIDs. This notebook demonstrates the reverse engineering of this mapping logic and allows to view which Elektron FID currently populates given CF_ field for a given RIC. This notebook also converts CF_DATE and CF_TIME fields from GMT to Windows timezone set on user's machine.

**Pre-requisites:** 

**Thomson Reuters Eikon** on Windows with access to [Eikon Data APIs](https://developers.refinitiv.com/eikon-data-apis)

**Required Python Packages:** eikon, xml, datetime, pytz, tzlocal, numpy, os
