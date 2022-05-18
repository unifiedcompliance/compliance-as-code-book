# Chapter Structure

Before we get going, it’s best to lay out the rhythm of this work. Compliance as Code _can_ be complicated, but if broken down into its parts, not so much. So, let’s lay out how every chapter is going to evolve.

## The Main Thing

Every chapter starts with _The Main Thing_. Steven Covey coined a phrase I like to live by “The Main Thing is to keep The Main Thing the main thing.” In other words – focus. Therefore, each chapter starts with the focus, the _message_ we want to convey for that chapter. This work overall represents a single concept, and each chapter delivers a message supporting that concept.

## Key terms

I _hate_ it when people use words I don’t know. Or even worse, use words _I thought_ I knew the meaning of, but in a different way. Following _The Main Thing_, our gallant editor will list for you all of the key terms used in the chapter, along with their definitions. Our editor will also share the links to those terms up at [ComplianceDictionary.com](https://compliancedictionary.com). We can’t convey the right message if we are speaking different languages.

## Checking in at Univest.VIP

Throughout this work we are going to strive to keep things real. And that includes – as close as possible – real-world situations, with real world tasks and real-world problems to be solved. In order to accomplish this, we are going to add a bit of a _story element_ to our writing. We are going to tell the story through the eyes of the staff at a small investment firm Univest.vip and our main protagonist there is Sarah Connors (bottom right).

![Univest's HQ office](../.gitbook/assets/0.png)

We think the best way to make this as real as possible is to explain how Compliance as Code fits into everyday work life through explaining the various tasks that Sarah and her compatriots undertake, including the pains those tasks cause. And yes, Univest.vip has a site, an upcoming app (you can’t get it yet), and Sarah’s email is [sconnors@univest.vip](mailto:sconnors@univest.vip). _Sarah and her compatriots_ are an amalgam of people we know, people who have shared their tasks, pains, and gains they want to accomplish.

### The task(s) at hand

Compliance as Code doesn’t exist in a vacuum. It exists _to help us_ (and machines) become, and stay, compliant. In other words, it helps us _do_ something, or some things. So, once we have our language down, we need to look at the task(s) at hand, the pains those jobs cause, and the gains we want to accomplish. Only then can we see where Compliance as Code fits (or has yet to fit) into that picture. We will present our jobs/pains/gains as a table, ripped off from the folks at [Strategyzer](https://www.strategyzer.com/business-model-canvas/value-propositions)[\[1\]](broken-reference). Here’s a sample below, wherein each individual job will be listed, along with that job’s associated pain(s) and gain(s).

| **Task**           | **Pain(s)**                            |
| ------------------ | -------------------------------------- |
| The job goes here. | The list of pains goes here.           |
| ****               | **Gain(s)**                            |
|                    | The list of potential gains goes here. |

## The current situation

Once we know the job(s) that people must do, we’ll look at the current situation, starting with the existing structure of the data and the structure of any current APIs and tools that can help us out.

### The use of JSON in our discussions

When discussing any of the data structures, we are going to be using the JSON-LD data format to do so. JSON (or JavaScript Object Notation) is a highly portable data interchange format. While its structure is recognized natively by Javascript, its formatting conventions are easily recognized by other C-like languages. JSON is built on two universal data structures:

* A collection of name/value pairs. In various languages, this is realized as an object, record, struct, dictionary, hash table, keyed list, or associative array.
* An ordered list of values. In most languages, this is realized as an array, vector, list, or sequence.

These are universal data structures. Virtually all modern programming languages support them in one form or another. It makes sense that a data format that is interchangeable with programming languages also be based on these structures. In JSON, they take on these forms:

* An object is an unordered set of name/value pairs. An object begins with and ends with } (right brace). Each name is followed by a colon “:” and the name/value pairs are separated by commas “,”.
* An array is an ordered collection of values. An array begins with a left bracket “\[“ and ends with a right bracket “]”. Values are separated by a comma “,”.
* A value can be a string in double quotes, or a number, or true or false or null, or an object or an array. These structures can be nested.
* A string is a collection of zero or more Unicode characters, wrapped in double quotes, using backslash escapes. A character is represented as a single character string.

Excepting a few encoding details, that completely describes the language. If you are comfortable with this, great. If you need a bit of a refresher on how we got to JSON, how it differs from spreadsheets and SQL, then please read XXX.

### The various JSON schemas that might be at play

There are at least twenty different Compliance as Code schemas in play today. Each of these schemas intersect at various points with our discussions here. We’ve listed each of the schemas in the section _The interpretations of Compliance as Code_ in this document. _If_ a schema has something to do with the topic at hand, we will cover the schema and it plays out for that topic. If not, we will ignore it in that discussion.

## The solution(s)

There’s where we are at, and where we want to be. Once we know what the problem is and where we are, we’ll focus on how to get to _where we want to be_. The breakdown for the solutions will be presented thusly:

### The GRCSchema.org schema

This schema is the structure you’ll need to understand going forward. This won’t be an _in-depth_ look at the schema, but rather an overview of the [key points](https://docs.grcschema.org/)[\[2\]](broken-reference).

### The tools/methods for how to get there

Here’s where we turn the pains into pain relievers. Here is where we also add gain creators (if there are any).

### The Styles

Once we understand the schema and the tools, if necessary, we’ll also go through key points of the styles in question when working with this schema. Yes, styles are important. Much like the schema, we won’t go into depth about the styles, as those are covered [online](https://stylemanual.grcschema.org/)[\[3\]](broken-reference). We’ll focus on _specific aspects_ we need to deal with now.

## Footnotes

1. &#x20;[https://www.strategyzer.com/business-model-canvas/value-propositions](https://www.strategyzer.com/business-model-canvas/value-propositions) [↑](broken-reference)
2. &#x20;All schemas for GRCschema.org are presented in JSON-LD format at [https://grcschema.org](https://grcschema.org/) and fully documented at [https://docs.grcschema.org](https://docs.grcschema.org/). [↑](broken-reference)
3. &#x20;The full style manual is found at [https://stylemanual.grcschema.org](https://stylemanual.grcschema.org/). [↑](broken-reference)
