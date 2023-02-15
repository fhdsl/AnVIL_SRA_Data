
# Multiple SRA files {#multiple-sra-files}

More than likely, you will be importing multiple files from SRA. Luckily, this is quite easy in AnVIL! In contrast to how your local computer works, The SRA Fetch Workflow imports files in parallel, so it does not take a substantially longer time.

## Select Workflow Data

Navigate to the WORKFLOWS Tab and select the SRA_Fetch Workflow.

<img src="02-multi_file_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g1f25a933000_0_0.png" title="Workflows tab with SRA_Fetch." alt="Workflows tab with SRA_Fetch." width="100%" style="display: block; margin: auto;" />

Select "Run workflow(s) with inputs defined by data table".

<img src="02-multi_file_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g1f25a933000_0_10.png" title="'Run workflow(s) with inputs defined by data table' has been selected." alt="'Run workflow(s) with inputs defined by data table' has been selected." width="100%" style="display: block; margin: auto;" />

Set the "Select root entity type" to "sample" and click SELECT DATA.

<img src="02-multi_file_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_0.png" title="Step 1 and 2 for setting up the Workflow." alt="Step 1 and 2 for setting up the Workflow." width="100%" style="display: block; margin: auto;" />

Select the second through fifth samples and click OK on the bottom right.

<img src="02-multi_file_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_54.png" title="Select multiple files from the sample table" alt="Select multiple files from the sample table" width="100%" style="display: block; margin: auto;" />

Ensure the "Attribute" is set to `this.sample_id` and click RUN ANALYSIS.

<img src="02-multi_file_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_64.png" title="Confirm `this.sample_id` and click the RUN ANALYSIS button" alt="Confirm `this.sample_id` and click the RUN ANALYSIS button" width="100%" style="display: block; margin: auto;" />

Click LAUNCH. You can close your browser or shut down your computer without interrupting the transfer.

<img src="02-multi_file_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_73.png" title="Click the LAUNCH button; the 4 analyses being run is called out" alt="Click the LAUNCH button; the 4 analyses being run is called out" width="100%" style="display: block; margin: auto;" />

::: {.notice}
The Workflow knows that you probably want to parallelize the import of your SRA files. This means that each import is happening at the same time. Notice how this workflow with multiple samples actually launched 4 different jobs/analyses! This means that AnVIL can help you process lots of files much faster than working with them one by one.
:::

## Check Workflow

Click on the JOB HISTORY tab. Different submissions are arranged by newest on the top. You should see that the job status is "Done".

<img src="02-multi_file_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_83.png" title="An arrow pointing to 'Done' indicates the Workflow has completed successfully" alt="An arrow pointing to 'Done' indicates the Workflow has completed successfully" width="100%" style="display: block; margin: auto;" />


## Locate Data

Click on the DATA tab and click on the "sample" table on the left.

<img src="02-multi_file_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_31.png" title="Navigate to the Files folder under the DATA tab" alt="Navigate to the Files folder under the DATA tab" width="100%" style="display: block; margin: auto;" />

You should now see the files associated with the second through fifth sample!

<img src="02-multi_file_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_92.png" title="The imported files are now visible in the sample table" alt="The imported files are now visible in the sample table" width="100%" style="display: block; margin: auto;" />

## Summary

- Go to the WORKFLOWS tab
- Select **multiple** samples via data table ("Run workflow(s) with inputs defined by data table")
- Set the Attribute to `this.sample_id`
- SAVE and RUN ANALYSIS
- Go to DATA tab and click "sample" table to see files populated
