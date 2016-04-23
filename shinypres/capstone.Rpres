<style>
/* Remove auto-hyphenation */
.reveal h1, .reveal h2, .reveal h3 {
  word-wrap: normal;
  -moz-hyphens: none;
}

/* Slide titles */
.reveal h3 {
  font-size: 50px;
  color: blue;
}

/* Heading for slides with two hashes ## */
.reveal .slides section .slideContent h2 {
  font-size: 40px;
  font-weight: bold;
  color: green;
}

/* Ordered and Unordered list styles */
.reveal ul, .reveal ol {
  font-size: 30px;
  color: black;
  list-style-type: round;
}
</style>

nextWord prediction app
========================================================
author: VeryFatBoy
date: 24 April 2016
autosize: true
font-family: 'Arial'
transition: zoom
incremental: true

<small>This presentation is also available at:</small>

<small><http://rpubs.com/VeryFatBoy/capstone></small>

<small>Presentation source files available at:</small>

<small><https://github.com/VeryFatBoy/capstone/></small>

The opportunity -- nextWord prediction app
========================================================

- Tremendous word-wide growth in smart phones and tablets
- Fast-paced world where people want to save time and effort typing
- Huge world-wide English-speaking market
- Great opportunities for additional language development
- Tremendous investor interest and funding potential
- Shiny beta release available today -- awaiting reviewer feedback!

Application development
========================================================

- Ingest data from three files: blog posts, news articles, twitter posts
- Create training and test data
- 40% sample for training data from each file, then combine to create corpus
- Corpus cleanup: punctuation, numbers, whitespace, convert to lower-case, and so on
- Create n-grams: unigrams, bigrams and trigrams
- Use packages **tm**, **tau** and roll-your-own approach
- N-gram tables saved in .RDS files

Application use
========================================================

- Read .RDS files at startup
- User input cleanup: punctuation, numbers, whitespace, convert to lower-case, and so on
- Take last two words from input, apply Katz Backoff algorithm
    - <strong>trigram:</strong> P(obama | president, barack) if C("president barack obama") > 0
    - <strong>bigram:</strong> P(obama | barack) if C("barack obama") > 0
    - <strong>unigram:</strong> P(obama)
- Each distribution needs a factor
    - P(obama | president, barack) = alpha(obama, barack) * P(obama | barack)
- Calculate probabilities, sort results, render next word, table and chart

Summary
========================================================

![Beta Image](www/screen.jpg)

- Beta version available today!
- Awaiting reviewer feedback for enhancements and suggestions
- Try it at: <https://veryfatboy.shinyapps.io/capstone/>
