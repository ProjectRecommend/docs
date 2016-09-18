# Software Requirements Specification

    Product : Project Recommend
    Description : An offline music recommendation system
    Status : Approved
    Development Status  : design phase
    Author : Surajnath Sidh

----

# Revisions

### Latest
    Current Version : 0.1
    Current Status : Work in Progress
    Date : 14-09-2016

### Revision History
- Version 0.0
    - Date : 14-09-2016
    - Reason For Changes : initial changes

----

# Table of Contents

##### 1
- 1.1 Purpose
- 1.2 Document Conventions
- 1.3 Intended Audience and Reading Suggestions
- 1.4 Product Scope
- 1.5 References

##### 2
- 2.1 Product Perspective
- 2.2 Product Functions
- 2.3 User Classes and Characteristics
- 2.4 Operating Environment
- 2.5 Design and Implementation Constraints
- 2.6 User Documentation
- 2.7 Assumptions and Dependencies

##### 3
- 3.1 User Interfaces
- 3.2 Hardware Interfaces
- 3.3 Software Interfaces
- 3.4 Communications Interfaces

##### 4
- 4.1 System Feature 1
- 4.2 System Feature 2 (and so on)

##### 5
- 5.1 Performance Requirements
- 5.2 Safety Requirements
- 5.3 Security Requirements
- 5.4 Software Quality Attributes
- 5.5 Business Rules

##### Appendix
- Appendix A: Glossary
- Appendix B: Analysis Models
- Appendix C: To Be Determined List

----


# 1 Introduction

## 1.1 Purpose

Project Recommend is project to provide recommendation on your offline music collection that you have
in your computer locally.
This document describes Full system but it's emphasis is on Core part of system aka recommendation system

## 1.2 Document Conventions

- TBD - to be decided
- WIP - work in progress


## 1.3 Intended Audience and Reading Suggestions

This document is intended for Developers, Software architects, Testers, Project managers and Documentation Writers.
But anyone with programming background and some experience with UML can understand this document.

## 1.4 Product Scope

This software aims to solve the basic problem of providing recommendation on all of your offline music collection
it has some extra benefits like
- it works with low bandwidth connections
- it is not platform or service specific
- it is not bounded with any music provider services so it is suggestions are not limited to particular service

## 1.5 References

- TBD

# 2.Overall Description

## 2.1 Product Perspective

- This is self contained product

## 2.2 Product Functions

- can listen to songs
- play, pause, forward playing songs
- get recommendation on songs
- update metadata of songs

## 2.3 User Classes and Characteristics

TODO - will be added after class diagram

## 2.4 Operating Environment

System Requirements
- Anything that can play music and have any of mentioned OS installed
- internet Connection is required for suggestions

OS
- GNU/Linux
- Windows
- MacOS


## 2.5 Design and Implementation Constraints

TODO

## 2.6 User Documentation

Basic guide on How to use software will be available online and shipped with software help as well.
Software Source code will also be available along with it's Documentation under suitable Open Source license


## 2.7 Assumptions and Dependencies

TODO

# 3 External Interface Requirements

## 3.1 User Interfaces

TODO

## 3.2 Hardware Interfaces

TODO

## 3.3 Software Interfaces

TODO

## 3.4 Communications Interfaces

TODO

# 4 System Features

## 4.1 System Feature 1

TODO

#### 4.1.1 Description and Priority

TODO

#### 4.1.2 Stimulus/Response Sequences

TODO

#### 4.1.3 Functional Requirements

TODO

## 4.2 System Feature 2 (and so on)

TODO

----

# 5. Other Nonfunctional Requirements

## 5.1 Performance Requirements

- System will be fast enough to play music without any shattering or buffering, otherwise
that will result in undesirable experience.
- System will be robust to deal and act accordingly  with common error scenarios like no
internet connection, unavailable metadata, unsupported file types.
- In case of failures it should be able to fail or recover gracefully.
- System will be usable and fast enough to response to user action or give feedback to action, ideally under 1/60 second hence achieving 60 Frames Per Second.


## 5.2 Safety Requirements

- In scenario when there is not enough data to automatically tag Metadata we rely [AcoustID](https://acoustid.org/) and [MusicBrainz](https://musicbrainz.org/) for metadata
based on AcoustID fingerprint, in some but rare scenarios it can result in incorrect metadata of song,
to prevent that scenarios user can manually edit metadata of songs when it see an incorrect tagged song

## 5.3 Security Requirements

- Connection between user and [MusicBrainz](https://musicbrainz.org/) servers should be Encrypted (HTTPS/TLS).

## 5.4 Software Quality Attributes

- System will not leak memory.
- System will peacefully co-exist with other software
- System will not cause or trigger any events that will leave Operating System in unrecoverable state

## 5.5 Business Rules

- This software is an Open Source software.
- Unless required by applicable law or agreed to in writing, software distributed is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.

----

# 6. Appendix

# 6. Other Requirements

TODO


## Appendix A: Glossary

TODO

## Appendix B: Analysis Models

TODO

## Appendix C: To Be Determined List

TODO

----
# Comments
