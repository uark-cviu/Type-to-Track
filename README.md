# Type-to-Track: Retrieve Any Object via Prompt-based Tracking (NeurIPS 2023)

[**Type-to-Track: Retrieve Any Object via Prompt-based Tracking**](https://arxiv.org/abs/2305.13495)

[Pha Nguyen](https://pha-nguyen.github.io/), [Kha Gia Quach](https://scholar.google.com/citations?user=AQ-4ioEAAAAJ), [Kris Kitani](https://www.cs.cmu.edu/~kkitani/), [Khoa Luu](https://scholar.google.com/citations?user=JPAl8-gAAAAJ)

In NeurIPS, 2023.

<video src="https://uark-cviu.github.io/Type-to-Track/static/videos/teaser_mot.mp4"></video>

**The responsive _Type-to-Track_:** The user provides a video sequence and a prompting request. During tracking, the system is able to discriminate appearance attributes to track the target subjects accordingly and iteratively responds to the user's tracking request. Each box color represents a unique identity.

Abstract
--------

One of the recent trends in vision problems is to use natural language captions to describe the objects of interest. This approach can overcome some limitations of traditional methods that rely on bounding boxes or category annotations. This paper introduces a novel paradigm for Multiple Object Tracking called _Type-to-Track_, which allows users to track objects in videos by typing natural language descriptions. We present a new dataset for that Grounded Multiple Object Tracking task, called _GroOT_, that contains videos with various types of objects and their corresponding textual captions describing their appearance and action in detail. Additionally, we introduce two new evaluation protocols and formulate evaluation metrics specifically for this task. We develop a new efficient method that models a transformer-based eMbed-ENcoDE-extRact framework (_MENDER_) using the third-order tensor decomposition. The experiments in five scenarios show that our _MENDER_ approach outperforms another two-stage design in terms of accuracy and efficiency, up to 14.7% accuracy and 4× speed faster.

Introduction
------------

_GroOT_ contains videos with various types of objects and their corresponding textual captions of 256K words describing their appearance and action in detail. To cover a diverse range of scenes, _GroOT_ was created using official videos and bounding box annotations from the MOT17, TAO and MOT20.

Here are examples of what's annotated on videos of the GroOT dataset:

<video src="https://uark-cviu.github.io/Type-to-Track/static/videos/teaser_data.mp4"></video>


Annotations
-----------

v1.0:
-----

*   Category **name**, **synonyms** and **definition**: [\[Categories\]](./annotations/v1.0/categories.json)

*   Compatible with [MOT17](https://motchallenge.net/data/MOT17), [TAO](https://taodataset.org/) and [MOT20](https://motchallenge.net/data/MOT20)

*   Tracklet **captions**:
    *   [MOT17](https://motchallenge.net/data/MOT17) subset: [\[Train annotations\]](./annotations/v1.0/mot17_train_coco.json), [\[Sub-optimal test annotations\]](./annotations/v1.0/mot17_test_coco.json)
    *   [TAO](https://taodataset.org/) subset: _Under assessment_
*   Object **retrieval**:
    *   [TAO](https://taodataset.org/) subset: _Under assessment_

Notes:
------

*   Test annotation for tracklet **captions** of MOT17 is a sub-optimal ground truth. That is the raw tracking data of the best-performant tracker at the time we constructed the annotations (i.e. [BoT-SORT](https://motchallenge.net/method/MOT=5621&chl=10) at 80.5% MOTA and 80.2% IDF1).
*   The \`captions' field includes the first caption for appearance and the second for action. Any missing captions have been filled with a \`None' value.
*   The physical characteristics of a person or their personal accessories, such as their clothing, bag color, and hair color are considered to be part of their appearance. Therefore, the appearance captions include verbs carrying or holding to describe personal accessories.

Licensing:
----------

The annotations of _GroOT_, as well as the original source videos of MOT17 and TAO, are released under a [CC BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/) license per their creators. See [motchallenge.net](https://motchallenge.net/) for details.

BibTeX
------

    
    @article{nguyen2023type,
        title        = {Type-to-Track: Retrieve Any Object via Prompt-based Tracking},
        author       = {Nguyen, Pha and Quach, Kha Gia and Kitani, Kris and Luu, Khoa},  
        journal      = {Advances in Neural Information Processing Systems},
        year         = 2023
    }

This page was built using the [Academic Project Page Template](https://github.com/eliahuhorwitz/Academic-project-page-template).  
This website is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).