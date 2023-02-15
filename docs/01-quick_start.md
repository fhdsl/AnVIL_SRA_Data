# (PART\*) SRA ON AnVIL {-}




# Quick Start

In this module, we'll bring some metagenomic data into AnVIL.

This data comes from [this BioProject](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA904247), which collected soil samples to study bacterial communities in tallgrass prairie. Bacteria play an important role in this ecosystem, but can be changed by disturbance, management, and the presence of herbivores.

The SRA Data corresponding to this project is located [here](https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRP409181&o=acc_s%3Aa).

## Clone Workspace

Clone the Workspace `https://anvil.terra.bio/#workspaces/anvil-outreach/SRA-data-on-AnVIL`.

For this demo, we have given the cloned Workspace the name `SRA-data-on-AnVIL-example`.

## Set Up Samples

Navigate to the WORKFLOWS Tab and select the SRA_Fetch Workflow.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g1f25a933000_0_0.png" title="Workflows tab with SRA_Fetch." alt="Workflows tab with SRA_Fetch." width="100%" style="display: block; margin: auto;" />

Select "Run workflow(s) with inputs defined by data table".

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g1f25a933000_0_10.png" title="'Run workflow(s) with inputs defined by data table' has been selected." alt="'Run workflow(s) with inputs defined by data table' has been selected." width="100%" style="display: block; margin: auto;" />

Set the "Select root entity type" to "sample" and click SELECT DATA.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_0.png" title="Step 1 and 2 for setting up the Workflow." alt="Step 1 and 2 for setting up the Workflow." width="100%" style="display: block; margin: auto;" />

On the Select Data popup, select only the first sample, `SRR22375322`, and click OK.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_8.png" title="The first sample selected from the data table." alt="The first sample selected from the data table." width="100%" style="display: block; margin: auto;" />

## Launch Workflow

Click on the space underneath "Attribute" and select `this.sample_id`.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_17.png" title="'this.sample_id' must be selected under the Workflow Attribute" alt="'this.sample_id' must be selected under the Workflow Attribute" width="100%" style="display: block; margin: auto;" />

Click SAVE.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_26.png" title="The SAVE button is highlighted" alt="The SAVE button is highlighted" width="100%" style="display: block; margin: auto;" />

You are ready to launch the Workflow! Click RUN ANALYSIS.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_34.png" title="The RUN ANALYSIS button is highlighted" alt="The RUN ANALYSIS button is highlighted" width="100%" style="display: block; margin: auto;" />

Voilà! Your Workflow is running. 

::: {.notice}
Because the Workflow is happening in the cloud, you can close your browser or shut down your computer without interrupting the transfer.
:::

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_42.png" title="The Workflow status page describes submission statistics and job status" alt="The Workflow status page describes submission statistics and job status" width="100%" style="display: block; margin: auto;" />

## Check Workflow

Click on the JOB HISTORY tab. You should see that the job status is "Done". This might take a few minutes.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_50.png" title="The check mark indicates the Workflow has completed successfully" alt="The check mark indicates the Workflow has completed successfully" width="100%" style="display: block; margin: auto;" />

## Locate Data

Click on the DATA tab and click on the "sample" table on the left.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_31.png" title="Navigate to the Files folder under the DATA tab" alt="Navigate to the Files folder under the DATA tab" width="100%" style="display: block; margin: auto;" />

You should now see the file associated with the first sample!

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_41.png" title="The imported file is now visible in the sample table" alt="The imported file is now visible in the sample table" width="100%" style="display: block; margin: auto;" />

## Summary

- Clone [Workspace](https://anvil.terra.bio/#workspaces/anvil-outreach/SRA-data-on-AnVIL)
- Go to the WORKFLOWS tab
- Select sample via data table ("Run workflow(s) with inputs defined by data table")
- Set the Attribute to `this.sample_id`
- SAVE and RUN ANALYSIS
- Go to DATA tab and click "sample" table to see file populated

# Multiple SRA files

More than likely, you will be importing multiple files from SRA. Luckily, this is quite easy in AnVIL! In contrast to how your local computer works, The SRA Fetch Workflow imports files in parallel, so it does not take a substantially longer time.

## Select Workflow Data

Navigate to the WORKFLOWS Tab and select the SRA_Fetch Workflow.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g1f25a933000_0_0.png" title="Workflows tab with SRA_Fetch." alt="Workflows tab with SRA_Fetch." width="100%" style="display: block; margin: auto;" />

Select "Run workflow(s) with inputs defined by data table".

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g1f25a933000_0_10.png" title="'Run workflow(s) with inputs defined by data table' has been selected." alt="'Run workflow(s) with inputs defined by data table' has been selected." width="100%" style="display: block; margin: auto;" />

Set the "Select root entity type" to "sample" and click SELECT DATA.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_0.png" title="Step 1 and 2 for setting up the Workflow." alt="Step 1 and 2 for setting up the Workflow." width="100%" style="display: block; margin: auto;" />

Select the second through fifth samples and click OK on the bottom right.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_54.png" title="Select multiple files from the sample table" alt="Select multiple files from the sample table" width="100%" style="display: block; margin: auto;" />

Ensure the "Attribute" is set to `this.sample_id` and click RUN ANALYSIS.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_64.png" title="Confirm `this.sample_id` and click the RUN ANALYSIS button" alt="Confirm `this.sample_id` and click the RUN ANALYSIS button" width="100%" style="display: block; margin: auto;" />

Click LAUNCH. You can close your browser or shut down your computer without interrupting the transfer.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_73.png" title="Click the LAUNCH button; the 4 analyses being run is called out" alt="Click the LAUNCH button; the 4 analyses being run is called out" width="100%" style="display: block; margin: auto;" />

::: {.notice}
The Workflow knows that you probably want to parallelize the import of your SRA files. This means that each import is happening at the same time. Notice how this workflow with multiple samples actually launched 4 different jobs/analyses! This means that AnVIL can help you process lots of files much faster than working with them one by one.
:::

## Check Workflow

Click on the JOB HISTORY tab. Different submissions are arranged by newest on the top. You should see that the job status is "Done".

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_83.png" title="An arrow pointing to 'Done' indicates the Workflow has completed successfully" alt="An arrow pointing to 'Done' indicates the Workflow has completed successfully" width="100%" style="display: block; margin: auto;" />


## Locate Data

Click on the DATA tab and click on the "sample" table on the left.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_31.png" title="Navigate to the Files folder under the DATA tab" alt="Navigate to the Files folder under the DATA tab" width="100%" style="display: block; margin: auto;" />

You should now see the files associated with the second through fifth sample!

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_92.png" title="The imported files are now visible in the sample table" alt="The imported files are now visible in the sample table" width="100%" style="display: block; margin: auto;" />

## Summary

- Go to the WORKFLOWS tab
- Select **mutiple** samples via data table ("Run workflow(s) with inputs defined by data table")
- Set the Attribute to `this.sample_id`
- SAVE and RUN ANALYSIS
- Go to DATA tab and click "sample" table to see files populated
