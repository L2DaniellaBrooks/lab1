# Lab1
*This lab is copyrighted by Joshua Rest. Do not post any part of it online.*

## Structure of labs
This semester, you will be learning the skills to compare a gene family found in many different animals. Lectures will be focused on background material to understand the biology and analysis tools.
Each week in lab, we will all work together on a common gene family (HOX). 
Then you will conduct the same analysis on your own assigned gene family (AGF). You will use these labs to write a final paper about your AGF. 


## Keep track of your work on GitHub

Instructions and commands for each lab will be found here on GitHub; each lab you will create a repository from a template, just like you did today. The README document covers what you need to do for this analysis for GLOBINS. **You will post your answers to questions directly in this document [GitHub] and on blackboard [Blackboard]. In addition, you will need to document any commands, calculations or code you run here as a code book**. Your codebook will be  checked four time during the semester.

Github is a commercial site that hosts computer code (I'll just call them documents) for people like you and me who write code. It is a git - a type of version control - which means that each change to a document is recorded. In addition, it allows collaboration; people can check out or create a fork (separate version) of the code, and then work on it. For example,  this lab is a template of code that you put into your own repository to work on.

Here is a brief article describing what GitHub is and how it is used:
[https://kinsta.com/knowledgebase/what-is-github/](https://kinsta.com/knowledgebase/what-is-github/)

Here is a the first activity that GitHub suggests you do to get to know it: (not required for this lab, but please take a look).
[https://guides.github.com/activities/hello-world/](https://guides.github.com/activities/hello-world/)

README documents at GitHub, such as this one, are formatted in markdown language. Of course, you can just use plain text. But markdown  allows you to add pictures, format code and commands nicely, specify headings, etc. Here is github guide to markdown; please take a look at these instructions, so that you can use it to make your code book look nice:
[https://guides.github.com/features/mastering-markdown/](https://guides.github.com/features/mastering-markdown/)
In addition to creating markdown by hand,  we suggest you use the markdown editor hackmd [https://hackmd.io/](https://hackmd.io/). 
Look at the bottom of this document for a Markdown Cheat Sheet.

**The point of GitHub is to allow users to check out repositories (code and documents), make copies of them, edit them, and push those changes back to a central place, all while keeping track of every change.** GitHub is commonly used for writing, sharing, and collaborating on code, which is why we are using it in this class.

For today, you can edit this document directly where it is hosted in GitHub by clicking on the pencil in the upper right hand corner of this document. Then, copy and paste that code into a hackmd note. After editing in hackmd, copy and paste it back into the github window and save. **In order to save changes on GitHub, you need to press the commit button.** In a later lab, we will learn to check out the respository to a local machine, edit it, and push those changes back to GitHub.

## Part II. Gene exploration at NCBI       
NCBI (National Center for Biotechnology Information) hosts a website where biologists store and retrieve information about genes and genomes and lots of other biological information. By the end of this class, NCBI will be your best friend! NCBI is composed of many different databases, each describing a different aspect of a gene, genome, or protein. 

The goal of today’s lab is to get a feeling for the structure of a gene, and how you can retrieve information about a gene from NCBI. This semester, we will together study the HOX gene family. Together today, you will be exploring Genbank files describing the sequence of just one HOX gene, Hox-C5 LOC5514051 from the species *Nematostella vectensis* .
 
You can find a summary of the information available for this gene its Gene page by navigating to [ncbi](http://www.ncbi.nlm.nih.gov/gene) and typing 5514051 (its gene ID) in the search box.
Look down on the gene page, and you will see this graphical view of the scaffold. The gene is annotated below the scaffold:
![Gene View](https://share.sketchpad.app/22/ada-03e6-7819fe.png)

Please note that there are two transcript variants: X1 and X2. 
Think, discuss and look up: what is a transcript variant? 
Think, discuss, and look up: What is an isoform?
Think and discuss: What are the differences between transcript variants X1 and X2?

Why are we looking at a **scaffold** instead of a chromosome? This is a draft genome, which means that chunks of assembled DNA haven’t yet been assembled into whole chromosomes. These are called scaffolds. 

Clicking on the link that says "Genbank". 
This will bring you to the region of the genomic scaffold where our gene is located.

![Region of our gene](https://share.sketchpad.app/22/35d-c8f6-e4611d.png)

There are some really important things to pay attention to here.
You are on NEMVEscaffold_61. 
Currently, you are only seeing part of the scaffold - the part with the Hox-C5 gene. 
The selected region is:
```
717073..725925
```
Diccuss or look up what the term "scaffold" means.
Discuss or look up what this might look like if the gene were encoded on the complementary strand.

You can also see the length of this region:
```
8853 bp
```

Now, to see the entire scaffold, change the view to "whole sequence".

![Change Region Shown](https://share.sketchpad.app/22/24a-13bd-f0bea3.png)

> **[GitHub]  Make notes for yourself here about how you figured out the length of the entire scaffold. Use the edit button (little pencil in the upper right hand corner of the box) to directly edit the markdown here.** 

> **[Blackboard]  1. What is the length of the *entire* scaffold?**
8853
Go back to the region view on the scaffold for our Hox-C5 gene.

Find the **annotation of coordinates for the mRNA of transcript variant X1** within this region.  Specifically, the coordinates for the exons are provided by “join(…)”. Note the coordinates of the coding sequence (CDS) are also provided. You will need to compare the coordinates for the mRNA to the coordinates for the CDS to answer this question.

This is what is looks like:
```
     mRNA            join(1..669,2808..3183,6774..8853)
                     /gene="LOC5514051"
                     /product="homeobox protein Hox-C5, transcript variant X1"
```

> [Blackboard] 2. How many exons are there that make up the mRNA for Hox-C5 transcript variant X1? How many introns are there in the Genomic DNA, that are removed in the mature mRNA? 
> 3 exons, 2 introns 
> [GitHub] Make notes here about how you answered the question.
> counted the boxes (light green)
> [Blackboard] 3. What are the lengths of each of the first three exons for Hox-C5 transcript variant X1? The length of the second exon is calculated for you.
> [Github] Fill in your own calculations below.
```
Exon 1: 699-0= 699
Exon 2: 3183-2807 = 376bp
Exon 3: 8853-6773= 2080
```
> [Blackboard] 4. What are the lengths of each of the first two introns of Hox-C5 transcript variant X1? The length of the first intron is calculated for you.
> [Github] Fill in your own calculations below.
```
Intron 1: 2807-669 = 2138bp
Intron 2: 6773-3183= 3590

```
> **[Blackboard] 5. What is the total length of the mRNA for Hox-C5 transcript variant X1?**
> 3125
> **[GitHub] Show your calculations or notes below.**
*Hint: You could add up the length of all the exons, or you could navigate to the  mRNA molecule in Genbank.*
add all exons: 669+376+2080 (from question 3)
mRNA contains a 5’ UTR, the coding sequence, and a 3’ UTR. To calculate the length of the UTRs, we need to compare the mRNA to the CDS. To find the annotation for the coding sequence of Hox-C5 isoform X1, scroll down to the following annotation:
```
     CDS             join(664..669,2808..3183,6774..7174)
                     /gene="LOC5514051"
                     /note="Derived by automated computational analysis using
                     gene prediction method: Gnomon."
                     /codon_start=1
                     /product="homeobox protein Hox-C5 isoform X1"
```
>[Blackboard] 6. What exon does the coding sequence start in for Hox-C5 transcript variant X1?
>exon 1
>[GitHub] Show your notes here.
gen bank scroll to cds and it says start 664...669, falls within the 1...669 range 
>[Blackboard] 7. By comparing the coordinates of the mRNA and the CDS, calculate length of the 5’ UTR for Hox-C5 transcript variant X1. *Hint: the bases including the start of the mRNA and up to (but not including) the start of the CDS.*
>663
>[GitHub] Show your calculation here.

>[Blackboard] 8. By comparing the coordinates of the mRNA and the CDS, calculate length of the 3’ UTR for Hox-C5 transcript variant X1. *Hint: the bases after (but not including) the end of the CDS (i.e. after the stop codon), until the end of the mRNA.*
>1678
>[GitHub] Show your calculation here.
 
> [Blackboard] 9. What is the length of the coding sequence (CDS) in nucleotide base pairs (bp) for Hox-C5 transcript variant X1?
> 783
> [Github] Make edits here 
>
> [Blackboard] 10. How many codons are in the coding sequence for Hox-C5 transcript variant X1?
> 260
> [GitHub] Make notes here.
783-3/3 = 260
> [Blackboard] 11. How many amino acids are in the protein encoded for by   Hox-C5 transcript variant X1?
> [GitHub] Make notes here.

*Hint: the stop codon does not encode an amino acid.* 

> [Blackboard] 12. What are the first nine bases of the coding sequence (CDS) for Hox-C5 transcript variant X1?
> TYRGLUTYR
> [GitHub] Make notes here.
Example format for your answer: NNNNNNNNN
*Hint: An easy way to do this is to navigate to the mRNA page and click on "Highlight Features".*

> [Blackboard] 13. What are the amino acids (single letter code) encoded by these nucleotides? Example format for your answer: XXX.
> YEY

> [Blackboard] 14. Can you find the length of the introns from the mRNA and protein file? Why or why not? Recall that there are three different files we have looked at: (1) the genomic DNA file, (2) the mRNA file, (3) the protein file; review these files before answering the question.  Hint: the mRNA file always shows only fully spliced mRNA. either c or d


## Part III. Choose Your Gene Family
Now it's time to choose a gene family for your own term project.
To start, you will choose a *single gene* from that gene family. This is also a gene you will look at today. In a later lab, we will explore which gene family your gene is part of.
Hint: This gene family has *homologs* (gene copies) in many animal species, including humans. However, today, you will just be looking at a single copy in *Nematostella*. 
Choose a protein from the list here: https://docs.google.com/spreadsheets/d/1dydNUlaqDCmqGw6B1-XOyP9UNhIA8PDpvNYXFq8jtNM/edit?usp=sharing
Make sure to fill your name in to reserve the starting gene (and gene family) for yourself! Each person must work on their own.
*Suggestion:* Pick a gene that seems to have a known function, rather than an uncharacterized gene.
If there is a particular gene family you are interested in studying, ask your TA for help.

> [GitHub] What is the gene and protein you chose? 

Use this area to record information about *your gene* and the protein it encodes, including links that may be helpful and other things you find interesting.

Look up your gene at the genbank gene page.

[Blackboard] 15. What starting protein did you choose?
XP_001617744.2
[Blackboard] 16. What gene family does this starting protein belong to? 
sea anemone
[Blackboard] 17. How many isoforms does your starting protein have in Nematostella?
776
**Congratulations on completing Lab 1!**


# Markdown Cheat Sheet

Headers
---------------------------

# Header 1

## Header 2

### Header 3

Styling
---------------------------

*Emphasize*  _emphasize_

**Strong**  __strong__

==Marked text.==

~~Mistaken text.~~

> Quoted text.

H~2~O is a liquid.

2^10^ is 1024.

Lists
---------------------------

- Item
 * Item
 + Item

1. Item 1
2. Item 2
3. Item 3

- [ ] Incomplete item
- [x] Complete item

Links
---------------------------

A [link](http://example.com).

An image: ![Alt](img.jpg)

A sized image: ![Alt](img.jpg =60x50)

Code
---------------------------

Some `inline code`.

```
// A code block
var foo = 'bar';
```

```javascript
// An highlighted block
var foo = 'bar';
```

Tables
---------------------------

Item | Value
-------- | -----
Computer | $1600
Phone | $12
Pipe | $1 

| Column 1 | Column 2 |
|:--------:| -------------:|
| centered | right-aligned | 

Definition lists
---------------------------

Markdown
:  Text-to-HTML conversion tool Authors
:  John
:  Luke Footnotes
---------------------------

Some text with a footnote.[^1]

[^1]: The footnote.

Abbreviations
---------------------------

Markdown converts text to HTML.

*[HTML]: HyperText Markup Language

LaTeX math
---------------------------

The Gamma function satisfying $\Gamma(n) = (n-1)!\quad\forall
n\in\mathbb N$ is via the Euler integral

$$
\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.
$$