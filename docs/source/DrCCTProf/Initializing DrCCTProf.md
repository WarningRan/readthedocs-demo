# Initializing DRCCTLib

This step is to initialize DrCCTProf and register the custom instrumentation functions to monitor all or a subset of instructions.

Initialize DrCCTProf via `drcctlib_init_ex` with the following parameters:
- `filter`: an instruction filter;
- `file`: the file path of the source code of the guest program at the current point in the program.
- `func1`: an instrumentation function for instructions;
- `func2`: an instrumentation function the beginning of basic blocks;
- `func3`: an instrumentation function for the end of basic blocks;
- `flag`: a mode bitvector flag to tell DRCCTLib how to operate.

>***Advice:***  
After the initialization, you could use the function `drcctlib_exit(void)` to clean DRCCTLib.