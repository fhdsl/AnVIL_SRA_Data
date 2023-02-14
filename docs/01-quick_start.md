# (PART\*) SRA ON AnVIL {-}




# Quick Start

In this module, we'll bring some metagenomic data into AnVIL.

This data comes from [this BioProject](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA904247), which collected soil samples to study bacterial communities in tallgrass prairie. Bacteria play an important role in this ecosystem, but can be changed by disturbance, management, and the presence of herbivores.

The SRA Data corresponding to this project is located [here](https://www.ncbi.nlm.nih.gov/Traces/study/?acc=SRP409181&o=acc_s%3Aa).

## Clone

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

Click on the DATA tab and click on the "Files" folder on the bottom left. You should see a folder `submissions/`.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_78.png" title="Navigate to the Files folder under the DATA tab" alt="Navigate to the Files folder under the DATA tab" width="100%" style="display: block; margin: auto;" />

Click on:

1. `submissions/`
2. the folder corresponding to the Submission ID you just ran. Example: `c247972a-b661-4cef-ba67-caf1fde95c9b/`
3. `fetch_sra_to_fastq/`
4. the folder corresponding to the Workflow ID you just ran. Example: `98134693-8392-4064-b8dc-af518e567e9b/`
5. `call-fastq_dl_sra/`

You should now see the `.fastq` file associated with the Workflow. You should also see log files and other helpful output.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_88.png" title="The sequence fastq file" alt="The sequence fastq file" width="100%" style="display: block; margin: auto;" />

Click on the file and copy the Terminal download command. Paste this somewhere temporary for now, as it will make our life easier shortly!

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_132.png" title="Click the clipboard button to copy the download command" alt="Click the clipboard button to copy the download command" width="100%" style="display: block; margin: auto;" />

## Launch Cloud Environment

Create a new Jupyter analysis in the ANALYSES tab. Click the START button followed by the Jupyter button.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_78.png" title="Creating a Jupyter analysis file" alt="Creating a Jupyter analysis file" width="100%" style="display: block; margin: auto;" />

When prompted, fill in the name as `sra_analysis` and click CREATE ANALYSIS.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_111.png" title="Fill in a name and click CREATE ANALYSIS" alt="Fill in a name and click CREATE ANALYSIS" width="100%" style="display: block; margin: auto;" />

When prompted, click CREATE to launch the default cloud environment.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_122.png" title="Click CREATE to launch the default cloud environment" alt="Click CREATE to launch the default cloud environment" width="100%" style="display: block; margin: auto;" />

Click on the Terminal button. After waiting a few minutes, you can see that the Cloud environment is ready.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208af248fb0_0_142.png" title="Click on the OPEN button when the environment is ready" alt="Click on the OPEN button when the environment is ready" width="100%" style="display: block; margin: auto;" />

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_3.png" title="The Jupyter Terminal appears when the cloud environment is ready" alt="The Jupyter Terminal appears when the cloud environment is ready" width="100%" style="display: block; margin: auto;" />

## Move Data to Persistent Disk

In the Terminal, paste the command you copied from earlier and hit return. In our case, it will look like this (Yours will be different)

```
gsutil cp gs://fc-e07a98ef-7485-4f48-bd77-d8c463867ada/submissions/c247972a-b661-4cef-ba67-caf1fde95c9b/fetch_sra_to_fastq/98134693-8392-4064-b8dc-af518e567e9b/call-fastq_dl_sra/SRR22375322_1.fastq.gz .
```

You will see some dialog indicating that the file is downloading.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_3.png" title="The Jupyter Terminal appears when the cloud environment is ready" alt="The Jupyter Terminal appears when the cloud environment is ready" width="100%" style="display: block; margin: auto;" />

type `ls` and hit return to list files and confirm your sequence file is present.

<img src="resources/images/01-quick_start_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_21.png" title="We want to see the sequence file listed in the working directory" alt="We want to see the sequence file listed in the working directory" width="100%" style="display: block; margin: auto;" />

The file can now be analyzed in your cloud environment!

::: {.notice}
You just copied your file to your **Persistent Disk**. As long as you launch a cloud environment from this Workspace, this sequence file should be available!
:::