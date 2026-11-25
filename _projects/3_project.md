---
layout: page
title: Learning Subtle Features with Divide and Conquer
description: SpliCER, a self-supervised architecture that stops simple patterns from drowning out subtle, complex features.
importance: 3
category: Machine Learning
---

Self-supervised methods often learn shortcut solutions, where easy-to-learn patterns dominate and subtler features that matter for scientific discovery are missed. SpliCER (Split Component Embedding Registration) splits each image into sections and distils information from each section, guiding the model to learn complex features without losing simple ones.

It works with any self-supervised loss, can be added to existing methods without modification, and gave significant downstream improvements in both medical and geospatial imaging.

Paper: [arXiv:2503.07444](https://arxiv.org/abs/2503.07444). See also [publications](/publications/).
