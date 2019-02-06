# Architecture

## Table of Contents

* ### Introduction
    
* ### Architecture and Frameworks

* ### Basic Website Flow
    
## Introduction

This document serves as a way to clarify the software design of the Brewski++ website.  It will go into detail about the MVC architecture model, the frameworks needed to achieve this model, as well as a general use-case for Client-Side operation.

## Architecture and Frameworks

We are using a Model - View - Controller modular design for our website implementation.  For simplicity in this document, we will analyze these three modules separately and how they relate to the front-end and back-end view of our website.

![MVC Flow](https://i.imgur.com/FmBdfia.png "MVC Flow.png")

### Model (Database):

The Model is our database operations.  Only the Controller may connect with the database; the View should never be allowed to communicate with the database.  We will be adding beers to the user's database as they add them.

### View (Front-End):

This is our client-side operations that will be located in our "View" folder.  The View listens to the Controller and makes no decisions for itself.  We will be using JavaScript and HTML for these operations.  We will be performing our AJAX calls to the API in the front-end.

### Controller (Back-End):

The Controller is the middle-man between the View and Model.  The bulk of logical operations will be located in the "Controller" folder.  We will be using ASP.NET Core for these operations.

## Basic Website Flow 

![Brewski++ DFD](https://i.imgur.com/ipgFI22.png "Brewski++ DFD.png")


The Client enters information about a specific beer they have tried and adds it to a list.  The View sends these entries to the Controller.  The Controller communicates with the Model and information is stored here.  The Model confirms and directs back to the Controller which then leads back to the View.  The View sends confirmation to the User about their entry.  
