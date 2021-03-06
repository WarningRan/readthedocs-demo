## Obtain Full Calling Context

After you initialized DrCCTProf, the next step is to query the calling contexts and/or data objects for instructions of their choice.

The context handle is set via `drcctlib_get_context_handle` with the following parameters:
- `drcontext`: the context of the current instruction;
- `slot`: the slot relative to the basic block.

You can get the number of context handles:

```drcctlib_get_global_context_handle_num()```.

Given the context handle, you may access the calling context with a fixed depth via `drcctlib_get_cct` with the following parameters:
- `ctxt_hndl`: the context handle;
- `max_depth`: the assigned call path depth, not the full call path.

>***Advice:***  
If you do not use the context any more, you may free the memory space pointed to by `contxt_list`:

```drcctlib_free_cct(context_t *contxt_list);```

Given the context handle, you may also access full calling context:

 ```drcctlib_get_full_cct(context_handle_t ctxt_hndl);```

You may print all the information of the fixed handle by the function `drcctlib_print_ctxt_hndl_msg` with the following parameters:
- `file`: the path storing the output;
- `ctxt_hndl`: the fixed context handle;
- `print_asm`: whether to print by the assembly language or not;
- `print_file_path`: whether to print the full path or not.

You may also print the full calling context of the fixed handle and the assigned depth by the function:

 ```drcctlib_print_full_cct(file_t file, context_handle_t ctxt_hndl, bool print_asm, bool print_file_path, int max_depth);``` 
