# Background Information

## Folder Contents

This directory contains two folders `mcp` and `skills`. 

### The `mcp` Folder 

This folder contains a complete *MCP* server project from github. Information about the MCP server can be got by reading the usual files. The contents of the `mcp` folder are an input for guiding the work to be done by using Antigravity in this folder. **Do not change anything in the `mcp` folder**.

### The `skills` Folder

This folder is an *output* folder provided for holding the artifacts created by Antigravity. The contents of the `skills` folder may be modified or even deleted sometimes as Antigravity is used iteratively to obtain the desired results.

## Project Objective

The objective of this project is to create a set of skills (in the [Agent Skills](https://agentskills.io/home) format) that are functionally equivalent to the *tools* defined in the MCP server provided. All of the information needed for the creation of a skill is expected to be available in the code/documentation of the corresponding MCP tool. Do not use any information that is not available in the MCP implementation. All information gaps should be reported, and should stop Antigravity from proceeding further.

## Iterative and Incremental Process

The process of converting the MCP server's tools into a set of skills is expected to be iterative, addressing small bits of functionality at a time. There are many details to be addressed, so we expect to have many cycles of [experiment, review, re-strategise, modify-prompt] before we are ready to make that final perfect run. Be patient, don't do more than is necessary!

## Skill Implementations

Each skill implementation must be placed in a distinct folder with a suitable name, and must contain the mandatory `SKILL.md` file. The logic of the skill should be implemented as a Python script.

### `scripts` Sub-Folder

Each skill folder should also contain a `scripts` sub-folder. This sub-folder should contain a suitably named `.py` file in the format of a [Python shebang script](https://realpython.com/python-shebang/). 

#### Script Inputs

If a script takes just one mandatory argument as input, the script should access that input item as `sys.argv[0]`. 

But if a script takes more than one argument as input (or any of the arguments are optional), the script should use the argument passing (and coding) convention embodied in the [argparse](https://docs.python.org/3/library/argparse.html) module. 

Scripts must check the number of arguments provided, and issue detailed error messages as needed.

#### Script Outputs

If a script produces just one item of output, the raw, unadorned value of the result should be printed out. 

But if a script outputs more than one item, it should print out a JSON object. The JSON output may be structured as a single object or a list of objects as necessary.