---
layout: page
title: Improving Models of Routine Histopathology Data
description: Using advanced imaging and molecular data during training to improve models that only need H&E slides at inference.
img: assets/img/data_schematic.jpg
importance: 1
category: Machine Learning
---

Advanced imaging and molecular technologies generate rich, information-dense data, but cost and availability mean that routine H&E stains are what is used in practice. This project asks whether knowledge in the rich data can be distilled into models that only ever see H&E.

- **More from Less** showed that self-supervised learning can distil knowledge from information-dense data into models that only need information-sparse data for inference, making downstream classification comparable with a fully supervised baseline.
- **TriDeNT** (*Medical Image Analysis*, 2025) extends this to privileged data such as immunohistochemistry, spatial transcriptomics and expert nuclei annotations, with improvements of up to 101% on downstream tasks.
- **Synthetic privileged information** shows that when paired data does not exist, generating it synthetically can improve representation learning, with up to 4.4x error reduction against single-modality training.

See the [publications](/publications/) page for the full papers.
