# WaDiff
I'm in the process of tidying up the WADIFF code. Please note that it's not yet complete. The code is coming soon!

1. Generate test cases according to the specification
    ```
    cd spec2test
    python generate_tcs_main.py generation_configs/v19.json
    ```
    The generated test cases are located in `spec2test/generated_tcs/v19`

2. Instrument the runtimes under test
    You can follow the instructions in `CP910_Runtimes_Info` to clone and hook the runtimes under test in our experiments.

3. Run the tester
    1. We specify the paths to the runtimes under test in the `cp910_runtime_tester/get_impls_util/impl_paras_std.py`. If necessary, you need to update the path to the runtimes according to your test environment.
    2. Run testing
        ```
        cd cp910_runtime_tester
        python run_dir_std_testing_main.py ../generated_tcs/v19/tcs <the path storing the result>
        ```
