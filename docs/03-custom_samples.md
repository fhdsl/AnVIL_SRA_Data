
# Customize Samples

You will probably need to select different samples than the ones in this demo. 

We've created another workspace, `SRA-data-on-AnVIL-example2`, to demonstrate how to upload your own sample IDs.

If you go to the DATA tab, you'll notice the same samples (ending in 22-26). These are here because data tables are copied when you clone a workspace. However, let's add a second set of samples ending in 27-31.

<img src="03-custom_samples_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_101.png" title="The 'sample' data table has been cloned from the original Workspace, including the sample IDs" alt="The 'sample' data table has been cloned from the original Workspace, including the sample IDs" width="100%" style="display: block; margin: auto;" />

## Import Data

Click on IMPORT DATA and select "Upload TSV".

<img src="03-custom_samples_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_144.png" title="The IMPORT DATA button and 'Upload TSV' option" alt="The IMPORT DATA button and 'Upload TSV' option" width="100%" style="display: block; margin: auto;" />

This opens a popup that looks like this:

<img src="03-custom_samples_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_153.png" title="The popup is titled Import Data Table and has the option to click to select a .tsv file" alt="The popup is titled Import Data Table and has the option to click to select a .tsv file" width="100%" style="display: block; margin: auto;" />

However, let's take a moment to get acquainted with the new file we'll be uploading.

## The `samples.tsv` File

First, download the samples file here. You might have to right-click and "Save as".

[Download `samples.tsv`](https://raw.githubusercontent.com/fhdsl/AnVIL_SRA_Data/main/samples.tsv)

Next, open the file on your local machine. This is what it might look like in Microsoft Excel:

<img src="03-custom_samples_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_163.png" title="The samples we want to import from SRA are listed in rows in `samples.tsv`" alt="The samples we want to import from SRA are listed in rows in `samples.tsv`" width="100%" style="display: block; margin: auto;" />

::: {.notice}
The column header `entity:sample_id` is important. `entity:` is required. `samples` becomes the name of the data table. So for example, if our header was `entity:reference_id`, a data table called "reference" would be created in AnVIL. If you didn't want to overwrite anything in the original "samples" table, you could change the column header. As long as none of the IDs are the same, no data will be overwritten. 
:::

## Upload the TSV

Back on AnVIL, Click to select a TSV file. This file should be the one you just downloaded above called `samples.tsv`. You will see a warning about potentially overwriting the existing entries. We know that none of the IDs in the new samples file overlap, so click START IMPORT JOB.

<img src="03-custom_samples_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_171.png" title="The warning is now visible on the popup and the START IMPORT JOB button is highlighted" alt="The warning is now visible on the popup and the START IMPORT JOB button is highlighted" width="100%" style="display: block; margin: auto;" />

New samples have been added!

<img src="03-custom_samples_files/figure-html//1l0P0gFpsPkYG7blqJ_5JyYYlztJFZDD39CnIB4svrY8_g208b8f790dc_23_179.png" title="The new samples have been appended to the end of the samples data table" alt="The new samples have been appended to the end of the samples data table" width="100%" style="display: block; margin: auto;" />

::: {.notice}
You can now proceed with running the Workflow as you did in the [Quick Start](#quick-start) and [Multiple Files](#multiple-sra-files) sections.
:::

## Summary

- Go to the DATA tab
- Select IMPORT DATA and "Upload TSV"
- Add your custom file and click START IMPORT JOB
