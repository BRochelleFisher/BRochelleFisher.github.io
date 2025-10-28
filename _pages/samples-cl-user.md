---
layout: page
title: CL Project - User Docs
permalink: /samples/cl-user/
description: Controlled Language Project - User Documentation
nav: false
toc:
  sidebar: left
---

**Background**

I have a [personal project](https://github.com/BRochelleFisher/TWPortfolio/tree/main) to create and document how to make and maintain a proprietary controlled language. The in-progress dictionary is on [Google Drive](https://docs.google.com/spreadsheets/d/1Eqor-ys3PWhETH9ADSZiHAlgTcjmNn_oOX17rGmNh_o/edit?gid=29324754#gid=29324754).

This sample is the guide for technical writers or linguists who get the Dictionary from developers (see the technical sample for the Developer Guide).

---

# Simplifying Cybersecurity Documentation with a Proprietary Controlled Language

### Abstract

This version of the documentation is for technical writers or linguistic analysts. It assumes someone else ran the scripts that created your Dictionary. Your task is to work the words, making your Controlled Language dictionary.

**Copyright© 2025 Rochelle Fisher.** rochelle.fisher@gmail.com All Rights Reserved. Original work for private use. Content from collected samples belongs to their respective copyright owners.

**Sample Sources:**

- Rubicon Communications LLC. (Apr 25, 2025) netgate© Security Gateway Manual: Amazon AWS. © Copyright 2025 Rubicon Communications LLC.
- OpenCTI. (2025) OpenCTI User Guide: Manual Creations. © 2025 Filigran. All rights reserved.
- MISP. (2024) MISP User Guide: A Threat Sharing Platform. GPL and CC-BY-SA 4.0 international.

## Introduction to Controlled Languages

### What is a Controlled Language?

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

In technical writing, the taxonomy is usually for different audiences of a product, from marketing to technical: all &gt; C-level decision maker &gt; user &gt; advanced user &gt; system administrator. There will be a default CL, with all the rules that apply to all audiences, and a dictionary for each persona. For example, a taxonomy for a decision maker will be used mainly by Marketing and will allow the word `leverage` with the meaning "to use a foundation feature to reach the solution for which the product exists". For all other audiences, the word leverage is not allowed, and its alternative is `use`.

A Taxonomy Manager for a company that creates a shopping app for Smart Phones will be in charge of labeling strategies for search results. A Taxonomy Manager for a cybersecurity company will create a CL for different audiences and use a tool to enforce it.

This project is for one dictionary. To keep things simple in this guide, we will not use the word `taxonomy`. We will use the word `CL` (Controlled Language) for the default vocabulary and the rule set, or `dictionary` for the vocabulary alone.

## Workflow

These are the procedures in this project:

1. **Collect your documentation.** Save all the files together in one aggregate text file. Send this file to your Python developer.

   You will create a CL from your documentation. This project creates a CL for cybersecurity from online, GPL, or unlicensed content.

2. **Get the Dictionary file.**

3. **For each word, analyze usage** for the one definition, one part of speech, allowed or not allowed, audience, and examples.

4. **Out of scope:** Create grammar and content rules. Start with ASD-STE 100 rules and then customize as you require.

5. **Out of scope:** Select an AI tool, or create a Python script, to test content for CL conformance (we like writer.com).

---

## Getting Started with the Dictionary

### Work the First Words

The first words that you set up in your dictionary will be the easiest and will have the most impact.

**Prerequisites:** Have the dictionary file in a spreadsheet. Make sure it is sorted for COUNT.

**Effort:** This will require less than an hour.

#### To work through the most used words in your dictionary:

1. In the word with the highest count, set the Part of Speech (PoS).

   A typical result for the most used words are the names of your organization or product. ASD-STE calls these `technical names`. Set the PoS of the technical names in the top results as Name. This lets you filter for proper nouns which change more often than regular nouns.

   For example, the company name will change if your organization delivers a white label product.

2. Enter the PoS for the other most common words, such as `the that this from`. When you get to a word that is may be used in multiple parts of speech and is not a common word for all English content, skip it.

3. In the **Allowed** column, enter `T` (for true) or `F` (for false).

   Most of these first words will be allowed.

4. In the **Audience** column, enter `all` or select a persona from the list, if you are sure this word will be allowed only for this persona.

### Examples of the First Words

In our example, one of the product or company names is the word with the highest frequency. This should be your most used word too.

| Word                    | PoS  | Definition                     | Allowed? | Audience |
| ----------------------- | ---- | ------------------------------ | -------- | -------- |
| company or product name | Name | Add your marketing definition. | T        | all      |

In the top words, we have many that are clearly to be allowed: `this that will with from your`. These are pronouns, prepositions, and modular verbs. In a technical writing dictionary for native speakers, it does not give a lot of information to define the PoS. Is that a pronoun, adverb, conjunction, or determiner? Enter any reasonable value for the PoS.

In our style guide, we set a rule that we do not use minimalist rules. If `that` helps make a sentence easier to understand, we use it.

| Word   | Count | PoS         | Definition                     | Allowed? | Audience |
| ------ | ----- | ----------- | ------------------------------ | -------- | -------- |
| `this` | 730   | pronoun     | blank                          | T        | all      |
| `that` | 706   | pronoun     | blank                          | T        | all      |
| `will` | 667   | verb        | sets future tense of main verb | T        | all      |
| `with` | 612   | preposition | blank                          | T        | all      |
| `from` | 501   | preposition | blank                          | T        | all      |
| `your` | 376   | pronoun     | blank                          | T        | all      |

Note: We set an allowed definition for `will` to differentiate from its other definitions.

We have words that are industry standard for software technical writing: `introduction user data attributes attribute example organisation`.

- We set the PoS and Definition for our words. We set Allowed to T and Audience to all.
- Notice that `attribute` and `attributes` are two items.

  We restrict the values of the Word and ALT columns to one word or phrase, to prepare for a checker tool that might be a simple Python script. This is different from the way ASD-STE is written, but if you begin with this restriction, it will be easier later.

  If you know that you will use a specific AI-driven tool, such as Writer.com or jasper.ai, change the dictionary headers and values to work with the acquired tool.

- See `organisation`. We know we need this word, but this spelling is British. We know our rules will tell us to use American spelling. In this case, we will make a decision for our dictionary without analysis, or to put it more accurately, despite analysis. The spelling of `organisation` is the most commonly used form, but we will not use it. We will use the American spelling.

  1. Sort the complete range of dictionary alphabetically, by **Word**.
  2. Set `organization` and `organizations` as allowed (`T` in **Allowed**).
  3. Set the British `organisation` and `organisations` as not allowed (`F` in **Allowed**).
  4. In the allowed words, set the definition: `nonspecific body of people with a purpose`. We will use organization for a company, nonprofit org, military base, and all similar bodies.

  5. In **ALT1** for `organisation` and `organisations`, enter `organization` and `organizations`.

  When we sorted by Word to see all the issues of `organi*`, we saw `organizational`, with a **COUNT** of `1`. Why not add `organizational` on the fly? Answer: It is used only one time. We will analyze the text and find a more common rewrite in that one sentence. Or maybe that one instance is for `Organizational Unit (OU)` in Active Directory. If so, we will make that phrase a "word".

**NEXT:** When you are done with the most used words that you want to complete now (best practice: stop after an hour), sort the range by Count. We will analyze the words that are most likely to be NOT allowed: words used only one time. After that, go through the words in the order that best works for you.

---

## Analyzing the Next Words

You will analyze how your dictionary words are used in your sample.

#### To analyze words:

1. If you have a file created by the Context script, open it. It shows your words with 5 words before and after it, to see context.

   If you do not have that file and do not want to create it:

   a. Open the aggregated sample document (ask the developer who created the dictionary if you do not have it).

   b. Search for the word to analyze. We like to use Notepad++, to get all the results in a list, each result with context.

2. From the context, see if the word is used in more than one part of speech. If it is, and it is not obvious which is the most common, count the instances of each PoS.

   I usually paste or import the results in a spreadsheet and then use COUNTIF, filter, or pivot table.

3. See if the word, in the allowed PoS, is used with more than one definition. If it is, note the definitions.

   Use counts, industry standards, and internet searches to get the best definition. Get the ASD-STE 100 document and see what their dictionary says about the word. [NGRAM](https://books.google.com/ngrams/) is also a good tool.

4. See if the draft definition works in a large random sample, or in all uses. If you decide to make the word not allowed, see if the chosen alternate word or syntax works.

   **Best Practice:** When you write a definition, do not use the word in it. This will help you find words used as synonyms to replace with the allowed word. In a CL, each word has one definition, and each definition is represented by one word.

   **Example** Your documentation uses the past participles (past tense verb that functions as an adjective) `protected` and `secured` to mean the same thing. When you define them, the definition is _endpoint on which Product services run or network on which Product services run on all endpoints_. You decide that works for `protected`, but when you get to `secured`, you change the definition to be: _endpoint on which remediation ran to solve security vulnerability or exploit_. With these specific definitions, you can use both words, each with more meaning for the user.

   If you find that two or more words are used for the same definition and PoS, you must restrict your dictionary to only one. This will make it easier for users to read and to follow the instructions.

   **Example** You use `configure` to mean `enter` in a step like this: _Configure the IP address_. What is there to configure? Is it not enough to simply enter the IP address? Can you remove `configure` from your dictionary and use `set`, `enter`, and other more specific words for the action?

5. Update the rules, definition, and PoS. Enter good and bad examples.

   **Best practice**: You do not need a bad example for allowed words. It is best to use it for words that are not allowed. See ASD-STE 100 for examples.

6. If not allowed, make sure the words you set as alternatives are allowed and configured in the dictionary for PoS and definition, with examples.

### Examples of Word Analysis

Let's start with `organizational`.

#### To set `organizational` as a word in our CL:

1. Open the file with all your textual content. We named this file `sampleAgg.txt`.

2. Search for `organizational`.

   We found this sentence (owned by one of the organizations from which we used samples):

   > Produce intelligence that will be embedded into organizational workflows and would serve decision-makers.

3. When we analyze the use of `organizational`, we see ambiguity. Does the author mean that the workflows are organized? That they are for the organization? That there are different workflows for different groups in the hierarchy?

4. If we remove the word, it does not change the meaning, as far as we can see. We decide that this word is not allowed. If we had access to the SME, we would discuss their meaning and find alternatives.

   **Suggestion:** You have access to your SMEs. Set your CL words as best as you can. Then, discuss multiple words with similar issues. Edit your CL for alternative words and other decisions.

The next task is to work through the top words that are not obviously allowed or not allowed. Sort the dictionary by **Count**.

Our next word to work through is `event`.

#### Analyzing `event`:

1. Search for `event` in the sample content or context file.

   Our sample has 1417 results, for `event` and `events`.

2. Read the results. Make the definition draft. For example:

   > a security incident detected on the secured network

3. Fix the definition as you read more result lines.

   For example: The fifth result is for a procedure to create an event in the security application. We learn that an event always includes threat intelligence data and usage. We update the definition to:

   > object that contains a cybersecurity incident, report, or finding, with attributes, identifiers, and other data for analysis, prevention, and mitigation

   We see that event is used with other definitions.

   - **A system or user action** - This is a technical name for a specific product. For our general cybersecurity dictionary, it does not fit. We can communicate actions in errors and logs with their names, without the use of event.
   - **A phrase: "in the event this happens"** - This is a verbose phrase to mean `if`.
   - **CLI or API commands and pathnames.** Our checker tool must ignore code, filenames, and pathnames.

   This is an advantage of an XML technical writing tool. We can use elements that set content by type: `<code>`, `<codeblock>`, `<filename>`, `<pathname>`, and similar. We can then set the checker tool to ignore text in these elements. We add a rule to our style guide to use these elements.

4. Sort the dictionary by **Word**, to configure all similar words (plural with singular, commands, and so on).

5. In `event`, we enter the definition, good example, and bad example. In `events`, enter: `plural of event`.

6. A non-AI checker tool (and even some AI tools) cannot see the difference of meanings in the use of `event` with our specific definition or the use of the non-allowed definition. In **Rule**, enter: `Do not use to mean action of a user or server`.

   Our checker tool will show rules to help writers be consistent.

7. For the words that start with `event` and are obviously commands or pathnames, set the **PoS** to `command` and **Allowed** to `T`.

8. Add a row for the NOT allowed phrase `in the event` and make sure `if` is allowed.

**Dictionary Rows for event** (**Audience**: `all`, **Allowed**: `T` for each row)

| Word              | Definition                                                                                                                                               | PoS     | Rule / ALT1                                   |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- | --------------------------------------------- |
| `event`           | object that contains a cybersecurity incident, report, or finding, with attributes, identifiers, and other data for analysis, prevention, and mitigation | noun    | Do not use to mean action of a user or server |
| `events`          | plural of EVENT                                                                                                                                          | noun    | Do not use to mean action of a user or server |
| `eventblocklists` |                                                                                                                                                          | command |                                               |
| `eventgraph`      |                                                                                                                                                          | command |                                               |
| `eventid`         |                                                                                                                                                          | command |                                               |
| `eventinfo`       |                                                                                                                                                          | command |                                               |
| `eventreports`    |                                                                                                                                                          | command |                                               |
| `eventtag`        |                                                                                                                                                          | command |                                               |

**Dictionary Rows to Replace "in the event"**

| Word           | Count | Definition           | PoS         | Allowed? | Rule / ALT1                                                   |
| -------------- | ----- | -------------------- | ----------- | -------- | ------------------------------------------------------------- |
| `in the event` | 172   |                      | phrase      | F        | IF                                                            |
| `if`           | added | introduces condition | conjunction | T        | Separate the condition from the action or result with a comma |

#### Analyzing `type`:

This word is an excellent example. It is used in different parts of speech with different definitions in writing and native speaking. To control our written language, we must restrict this word to one PoS and one definition. Or we can decide to set it to not allowed, to be replaced with specific words.

1. Search for `type` in the sample.

2. Skim the hits with context. If it is not clear which PoS is mostly used, enter the PoS of each row.

   We found that it was most often used as a noun or technical name, but there were sentences with it used as a verb.

   > type yes when (verb)

   > Set the IPv4 Configuration Type to Static IPv4 (name)

   > corresponds to the desired type of instance (noun)

3. Add a row for type as a verb and set it to not allowed.

   **Dictionary Rows for type as a verb**

   | Word   | Count | Definition                    | PoS  | Good Example | Bad Example | Allowed? | Audience | Rule               | ALT1  |
   | ------ | ----- | ----------------------------- | ---- | ------------ | ----------- | -------- | -------- | ------------------ | ----- |
   | `type` | added | 1) to categorize; 2) to input | verb | enter yes    | type yes    | F        | all      | Do not use as verb | ENTER |

4. Make sure `enter` is allowed.

   **Dictionary Rows for enter**

   | Word  | Count | Definition      | PoS  | Good Example | Bad Example | Allowed? | Audience |
   | ----- | ----- | --------------- | ---- | ------------ | ----------- | -------- | -------- |
   | enter | added | to input values | verb | enter yes    |             | T        | all      |

5. We see that there many uses of `type` in the GUI and CLI.
   We could try to make it a technical name for user interface (UX) creators. The word `type` would be allowed in micro-copy and coding but not in technical writing. We would add a row for the UX persona in audience that would be **Allowed** for `type` as a `Name`. We would add another row for the other audiences that makes use of `type` as a noun not allowed.

   But we see in the results that `type` is used in text that cannot easily be rewritten. We must allow it for everyone, but only with the required definition, as an object in the product.

   **Dictionary Rows for type as a noun**

   | Word | Count | Definition                                           | PoS  | Good Example                                   | Bad Example                               | Allowed? | Audience | Rule                                                                         |
   | ---- | ----- | ---------------------------------------------------- | ---- | ---------------------------------------------- | ----------------------------------------- | -------- | -------- | ---------------------------------------------------------------------------- |
   | type | added | product group of objects with common characteristics | Name | some attribute types require associated events | some types of attributes are more complex | T        | all      | Do not use as general "kind"; use only as a category specific to the product |

6. Make sure the style guide rule that all text on the interface (GUI, API, or CLI) must be wrapped in an element, such as `<code>`, `<codeblock>`, `<guilabel>`.
   We can then set the checker tool to ignore text in these elements. If your checker tool shows the rules, it will not show this rule for interface labels, where it would cause user fatigue and be ignored when it is necessary.

7. We look through the uses of `type` to mean a general group of people or things having common characteristics. We can rewrite those.

   - **Given the text:**

     > supports various relationship types, and their usage depends on the entity types being linked

     This one sentence uses `type` with two definitions. The first can be removed. The second fits the allowed definition.

     **Controlled version:** _supports various relationships, and their usage requires linked entity types_

   - **Given the text:**

     > there are two types of admins: Org Admins and Site Admins

     The use of `type` is not required. If the SME does not like `level`, we can change it to a different word (`set`, `permissions`).

     **Controlled version:** _there are different admin levels: Org Admins and Site Admins_

   Note: We remove `two`. It is always best to not enumerate features, to make sure you do not create a conflict in the text when a new feature is added.

   - **Given the text:**

     > the type of storage used by Product can have an impact

     The full text discussed SSD devices and feed caching technology. We guess that `type` meant hardware and configuration.

     **Controlled version:** _The storage you use can have an impact._ OR _your storage hardware and algorithm can impact Product_ OR _storage hardware can impact Product_

## What Now?

You have a dictionary in progress. You must go through all the words, update the definitions and rules as you go.

When you are done with the top twenty or thirty words, sort your dictionary to see at the words with only one count. These words will be easy to set as not allowed, commands, or misspellings.

- If the word is not allowed, set its values. Make sure the alternative words are allowed.
- If the word is a command, in **PoS**, enter `command`. Set it to **Allowed** = `T`. Make sure your style guide says to wrap commands in relevant elements.
- If the word is a mistake, in **PoS**, enter `misspelling`. When your content is fixed for this mistake, you can remove it from the dictionary.
- If the word is correct and allowed, investigate. If it is a word for a specific audience, set it to **Allowed** = `T` for that audience. If a product owner or sponsor wants it for everyone, discuss why.

  For example, `absent` is used one time, in the phrase `absent a route`. This is a specific network configuration action. It is correct. We allow it for the user, sysadmin, and internal audiences. But we do not want it in the UX micro-copy or C-level marketing.

You will need a checker tool. You can acquire the tool before you complete the dictionary. You can ask a Python developer to make a script that returns an email or a webpage with results (unallowed words used, rules as reminders on allowed words, and unknown words). Or you can acquire an AI tool that integrates with your source CCMS. The important thing is that your dictionary is used. It is a dynamic tool for all content creators in your organization.
