---
layout: page
title: CL Project - C-Level Docs
permalink: /samples/cl-clevel/
description: Controlled Language Project - Executive Documentation
nav: false
toc:
  sidebar: left
---

**Background**

I have a [personal project](https://github.com/BRochelleFisher/TWPortfolio/tree/main) to create and document how to make and maintain a proprietary controlled language. The in-progress dictionary is on [Google Drive](https://docs.google.com/spreadsheets/d/1Eqor-ys3PWhETH9ADSZiHAlgTcjmNn_oOX17rGmNh_o/edit?gid=29324754#gid=29324754).

This sample is a short white paper for decision makers, to plan the initiative.

---

# Control Your Product Documentation

## _What is a Controlled Language and Why do you need it?_

### Abstract

This version of the documentation is for decision makers, concerned with documentation quality and translation costs.

---

## The Quality Gap is Painful

Your documentation is comprehensive and expensive, but it is not easy to read. It's expensive to translate, and it is too complex for non-native speakers to use without translation. It is too long and confusing.
Your organization has a style guide, but it does not seem to be enough.
You need a standard for simplicity and consistency.

## What is a Controlled Language?

A Controlled Language (CL) is set of rules for grammar, sentence length, and vocabulary. The rules define words and grammar as allowed or not allowed. This enforces consistency for all your documentation and conforms to or builds an industry standard for your products.

### Benefits of a CL

Adopting and enforcing a CL is the solution to many technical writing issues.

- For a team of writers, the CL enforces consistency of the content among the writers. If you have one writer, the CL enforces consistency over time among the documents.
- If you translate your content, the reduced vocabulary and grammar, and the re-use of matching content, makes translation significantly cheaper and often of better quality.
- For a product with a global market but without a budget for translation, the CL makes it easier for non-native speakers to read and use your documentation correctly. If your documentation is online, built-in machine translation (such as Google Translate) will give better results.
- With writer buy-in of the CL and re-use strategy, productivity will increase.
- Reduce your content by at least 30% without loss of information. Concise documentation makes it easier for users to find what is relevant to them at the time, makes clear to reviewers and stakeholders what is not relevant or incorrect, and makes the documented steps easier to follow.

### CL or Taxonomy?

In general terms, a taxonomy is a structured CL, with parents and children. For example, in biology the taxonomy has: class &gt; order &gt; family &gt; genus &gt; species.

In software and services, the taxonomy is usually for different audiences of a product, from marketing to technical: all &gt; C-level decision maker &gt; user &gt; advanced user &gt; system administrator. There will be a default dictionary (CL), with all the rules that apply to all audiences, and a dictionary for each persona.

For example, a taxonomy for a decision maker will be used mainly by Marketing and will allow the word `leverage` with the meaning "to use a foundation feature to reach the solution for which the product exists". For all other audiences, the word `leverage` is not allowed, and its alternative is `use`.

A Taxonomy Manager for a company that creates a shopping app for Smart Phones will be in charge of labeling strategies for search results. A Taxonomy Manager for a cybersecurity company will create a CL for different audiences and use a tool to enforce it.

This project is for one dictionary. To keep things simple in this guide, we will not use the word `taxonomy`. We will use the word `CL` (Controlled Language) for the default vocabulary and the rule set, or `dictionary` for the vocabulary alone.

---

## Project Tasks

### Task: Communicate

It is important that you communicate the purpose of the project to the technical writers. In the beginning all of the benefits are for the user. With time, it makes the work of the writers easier and faster.

**Expected Output:** Buy-in from the technical writers to be motivated to create the CL, to use it daily, to learn the rules, and to maintain changes as required.

**Owner:** Manager of Technical Writers or higher

**Est. Effort:** 1 - 5 hrs

---

### Task: Collect Documentation

Get the documentation that you have for one or more products. Save it all as one file, in txt format.

**Expected Output:** One aggregate text file of all documentation of a product

**Owner:** Technical Writer

**Est. Effort:** 5 - 9 hrs

---

### Task: Create Dictionary File

A developer or technical writer will run a set of Python scripts on the aggregate file. They will push the results to a spreadsheet and change it for specific column headings and valid data.

**Expected Output:** Spreadsheet with all unique words, the count of each word in your documentation, and columns for linguistic analysis

**Owner:** Developer (possible tech writer with Python experience)

**Est. Effort:** 1 - 4 hrs

---

### Task: Acquire or develop checker tool

Your technical writer researches the features and cost of tools, such as Writer and Jasper. If the cost is out of your budget for documentation, you will require the time and services of a developer. The technical writer should manage the developer's requirements and expected output.

The tech writer can begin working the Dictionary before the tool is acquired or created. If you acquire a tool before the writer begins, it may save some days that might be required to change the Dictionary structure to import properly to the tool.

**Expected Output:** A tool that will tell writers when they do not conform with the Dictionary, replacement words or content to rewrite, and rules that explain why. Most often, if you develop a tool in-house, it will not integrate with the authoring tool. Writers will get results only after they wrote a topic or book. If you acquire a tool, make sure it integrates with your authoring tool, for on-the-fly checks and fast rewrites.

**Owner:** Technical Writer / Decision-Maker

**Est. Effort:** Depends on solution

---

### Task: Create Vocabulary Values in Dictionary File

Technical writers analyze each unique word, in the spreadsheet or acquired tool. They set words and phrases as allowed or not allowed, create or update specific definitions, make sure there is one word for each definition and that each word has one meaning and one part of speech. They will add good and bad examples, rules for usage, and alternative allowed words for words that are not allowed.

**Expected Output:** A complete vocabulary to help writers remain consistent and to make sure content is controlled.

**Owner:** Technical Writer

**Est. Effort:** 20 words/hour. For a Dictionary with 10K - 50K words, and tech writers who work on it as a side project, plan for two work-years.
