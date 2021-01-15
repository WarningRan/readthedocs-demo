# Data-centric

Correlate contexts involved in the analyzed problem and accumulate metrics related to them. 

Typically, a map is used, where the key is a 64-bit entity formed out of two 32-bit context handles and the value is any metric.

??? Output the map as a tailored CCT with metrics for DrCCTProf's offline analysis with the following function:

`drcctlib_get_data_hndl(void *drcontext, void *address);`

