---
toc: true
layout: post
description: Brief overview of Streamlit and Agile Geoscience Kata.
categories: [streamlit]
title: Streamlit Example and Geo Kata
---
# Overview

Over the past few months I've been working through a [series of challenges (kata)](https://agilescientific.com/blog/2020/4/16/geoscientist-challenge-thyself?rq=kata) put together by the folks at [Agile Geosciences](https://agilescientific.com/). These are small, geoscience-oriented puzzles that are great for practicing basic Python skills and keep you thinking. I've also been doing a lot of my coding lately in [Streamlit](https://streamlit.io/) as opposed to [Jupyter Notebooks (or Lab)](https://jupyter.org/). This has been a good learning experience as Streamlit requires a bit more structured thinking in how you put your code together compared to Jupyter, where you can jump from cell to cell. Below I'll give a quick overview of my impressions of Streamlit and also give links to my Agile Geocomputing kata example solutions.

## Links to the Examples

If you want to jump right into examples, you can find go look at [my repository](https://github.com/armstrys/Kata-Geochallenge-Solutions). If you copy the [raw Github](https://help.data.world/hc/en-us/articles/115006300048-GitHub-how-to-find-the-sharable-download-URL-for-files-on-GitHub) link for a given `.py` file, then you can actually run the Streamlit code directly from the web. Try running the example below with an active environment that has Streamlit installed:

```
streamlit run https://raw.githubusercontent.com/armstrys/Kata-Geochallenge-Solutions/master/Kata-Prospecting.py
```

These were fun to put together and though the puzzles not inherently interactive, I tried to add a few buttons, sliders, and dropdowns along the way just to keep things interesting.

The [Streamlit Gallery](https://www.streamlit.io/gallery) is another good resource to see how community users are implementing projects in Streamlit. These examples show far more in-depth use-cases and the power of interactivity that Streamlit enables.

## An Overview of Streamlit

Streamlit is a really interesting product. It is a totally different take from Jupyter Notebooks on how to interact with your code. That has some big advantages, but a few drawbacks as well.

**Pros**

- Incredibly intuitive widgets. They just work. One line of code to assign a widget to a variable that can be used like any other variable.
- Code runs top to bottom every time it's executed, which is on save or by widget changes. This means no forgetting to re-run a cell in your notebook or accidentally re-running something that takes forever.
- Time-intensive code can be cached by placing `@st.cache()` above a function. This is a key optimization, because the way Streamlit executes your code.
- Can be used with any text editor.
- Designed to create applets quickly and easily - again, this is different than Jupyter Notebooks by design and it makes building clean interfaces with interactive widgets very straight-forward.

**Cons**

- More difficult to quickly test code and see results. The nature of the interface is not as natural as a Jupyter Notebook where each line of code spits out the result on the line below.
- Cannot render onto platforms like Github the same way you could a `.ipynb`.
- Finally, a bit more of a learning curve. This might not be as much of an issue for more experience coders. I found the friendly and forgiving sandbox of Jupyter Notebooks fundamentally easier to understand when getting started.

Initially, I planned to list a lack of third-party extensions on the Streamlit cons, but they have recently added a new feature called [Components](https://docs.streamlit.io/en/latest/streamlit_components.html) that allows for the addition of new components via custom HTML or Javascript. I don't have a good handle on what the limits or possibilities of this addition, but you can already view some of the early contributions using the new feature in their [components gallery](https://www.streamlit.io/components). If you haven't tried out Streamlit yet I hope this was enough useful info to convince you that you should give it a go (or not)!

# Conclusion

These puzzles and learning different coding styles in Streamlit have been a great help to my personal Python development over the past few months. While I will probably stick mostly with Jupyter Notebooks and Jupyter Lab due to the flexibility and interoperability with multiple platforms, Streamlit will be my go-to tool any time I have a simple POC that is better served as an applet than a live document.