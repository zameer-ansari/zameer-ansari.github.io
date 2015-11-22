---
layout: post
title: C# code documentation using visual studio
---

![Documentation please](http://www.webpal.net/blog/wp-content/uploads/2011/11/clutter_cartoon_3.png)

[courtesy](http://www.webpal.net/blog/tag/document-management-2/)

The golden rule of code documentation:

> Try to document [why](http://stackoverflow.com/a/4929769) (code design decisions) and avoid what (code design descriptions).

To keep up with the increasing complexity of the project, it's very important to document the coding decisions. It's one of the best practices.

[Visual studio](http://visualstudio.com) provides impressive ways for code documentation (and keeps the code understandable). It can also understand the changes that one make on hard code.

#Single or multi line comments

 - Short (or long) functional summary

	//single line comment

These are necessary to describe functionality in little.

	/*
	multiple 
	line
	comments
	*/

Avoid them. It is advisable to avoid writing essays about code. The end product shall be code not their long descriptions.

#Collapsible regions

 - Summary of the [functional block]()

	#region Short description about overall functionality of the code block

	//do stuff

	#endregion

Regions are collapsible. Just hover over the collapsed region and get a glance.

![Glance in collapsed code]()

#Summary

 - Summary of the function or property

        /// <summary>
        /// Summary description for the function or property goes here
        /// </summary>

 - Summary of the function parameter

        /// <param name="TestParameter">Summary description for the parameter goes here</param>

Visual studio changes this section after change of the parameter name.

![Change of parameters]()

 - Summary of the returning stuff

	/// <returns>Summary description for the function result goes here</returns>

A simple example:

    /// <summary>
    /// Main class of the project
    /// </summary>
    class Program
    {
        /// <summary>
        /// Main entry point of the program
        /// </summary>
        /// <param name="args">Command line args</param>
        static void Main(string[] args)
        {
            //Do stuff
        }
    }