---
layout: project
type: project
image: images/uw.png
title: Search Engine
permalink:
# All dates must be YYYY-MM-DD format!
date: 2017-11-29
labels:
  - Java
summary: I helped build a search engine for an assignemnt for CSE 373 at the University of Washington.
---

## Introduction

  While attending the University of Washington, I took CSE 373, Data Structures and Algorithms. The last assignents required students to build a basic search engine. All assignments allowed working with a classmate, so I worked together with a partner. To provide a ranking metric, we were to implement Term Frequency and Inverse Document Frequency (TF-IDF) ranking, which helped determine how "important" a given word is to a given document. Also, because there are websites that try to maximize search traffic by keyword stuffing, stuffing pages with as many different words and phrases possible, we were to implement a simple version of PageRank, an algorithm that computes the relative "importance" or "reputability" of a webpage based on what webpages link to it. In order to test our programs, we used a small set of Wikipedia pages.
 
## Example of Code

```ruby

/*
 * This method returns the tf scores for each document specified by pages.
 */
private IDictionary<URI, IDictionary<String, Double>> computeTfVectors(ISet<Webpage> pages) {
  IDictionary<URI, IDictionary<String, Double>> tfVectors = new ChainedHashDictionary<>();
  
	// For each page, create tf scores
	for (Webpage page: pages) {
	    URI uri = page.getUri();
	    IList<String> words = page.getWords();
	    
	    // Create tf scores for list of words in a page
	    IDictionary<String, Double> tfScores = computeTfScores(words);
	    tfVectors.put(uri, tfScores);
	}
	
	return tfVectors;
}

```
  
## What I learned

  This projects not only allowed me to improve my Java skills, but also experience working with another person. This was the first time I had collaborated with someone else for coding. I learned that it is very helpful to have another set of eyes to review your work. Often my partner would point out things that I would not have been able to see right away. I learned how to be a good team player, by working well individually, on my parts of the assignment, as well as with with others, when we came together and pieced together our programs. I will the carry the skills I've learned during this experience to my future endeavors.



