<div align=center>
  <h1>Software Design Document</h1>
  <h2>Project Recommend</h2>
  <b> Music Recommendation System </b><br />
  <b> Version <i>1.0</i></b>
</div><br /><br />

#### Team Project Recommend

- **Surajnath Sidh**  U101114FCS146
- **Rajdeep Mukherjee**  U101114FCS115
- **Raghav Mittal**  U101114FCS111
- **Pranshu Sahijwani**  U101114FCS104
- **S. Shakthi**  U101114FCS196
- **Saumya Gupta**  U101114FCS126

#### NIIT University
##### 26-Oct-2016

<hr/><br />


# Table of contents
1. Introduction

    1.1 Purpose of this document

    1.2 Scope of the development project

    1.3 Definitions, acronyms, and abbreviations

    1.4 References

    1.5 Overview of document

2. System architecture description

    2.1 Overview of modules / components

    2.2 Structure and relationships

    2.3 User interface issues

3. Detailed description of components

    3.1 Component template description

    3.2 X Component (or Class or Function ...)

    3.3 Y Component (or Class or Function ...)

    3.n Z Component (or Class or Function ...)

4.0 Reuse and relationships to other products

5.0 Design decisions and tradeoffs

6.0 Pseudocode for components

7.0 Appendices (if any)

SDS component template

<hr />

---------------------------------

# 2. System architecture description

Recommend (Our Software/System) is strictly based on modular architecture, there is four modules
in system that are functionally connected to each other as per Cohesion rules and these components
are Coupled as per Data coupling

## Coupling and Cohesion of System

#### Data Coupling

As per Definition one System have Data Coupling when *modules share data through, for example, parameters. Each datum is an elementary piece, and these are the only data shared (e.g., passing an integer to a function that computes a square root)*

From Sequence Diagram[todo - add link] we can see that System passes Data around hence system have Data Coupling.

#### Functional Cohesion

todo - add links to components

As per definition one system is in Functional Cohesion  *when parts of a module are grouped because they all contribute to a single well-defined task of the module*

as we can see that in our system each module contains classes that all contribute in a single Task.

- Music Player

    Music Player module handles functionality related to playing and handling music

- Local Storage

    Local Storage module functions as a Persistence Layer (Storage) of system.

- Meta Data

    Meta Data module handles all functionality related to Meta Data (ID3 Tags)

- Classifier

    Classifier handles all functionality related to Recommendation of songs for a songs



## 2.1 Overview of modules / components



## 2.2 Structure and relationships

## 2.3 User interface issues



---------------------------------

# Extras

# References

- [Cohesion](https://en.wikipedia.org/wiki/Cohesion_(computer_science)#Types_of_cohesion)

- [Coupling](https://en.wikipedia.org/wiki/Coupling_(computer_programming)#Types_of_coupling)
