Copyright (c) 2013, Phil Gooch. 
This software is licenced under the [GNU Library General Public License](http://www.gnu.org/copyleft/gpl.html) Version 3, 29 June 2007.

See LICENSE.txt file for license details.

* * * *


ClinicalMeasurements and TimeML Annotator
================================================

This plugin identifies quantitative and temporal concepts in clinical texts, and creates the following annotations

Date
Time
Duration
Frequency
Age
Measurement

It will also create TimeML[1] TIMEX annotations and features for Date, Duration and Frequency annotations.

It requires the Tagger_Numbers PR before it in the pipeline.

[1]: Pustejovsky J, Castan ̃o JM, Ingria R, Sauri R, Gaizauskas RJ, Setzer A et al. TimeML: Robust specification of event and temporal expressions in text. In New Directions in Question Answering, pages 28–34. AAAI Press, 2003.

How to use this plugin
=======================

ClinicalMeasurements is compatible with [GATE version 7.1](http://www.gate.ac.uk/) and higher. 
Simply create a Gazetteer instance, with case sensitivity set to 'false' and gazetteerFeatureSeparator set to ";", 
and point it the _measurement\_lists.def_ file in the 'gazetteer' folder, 
and create an instance of the JAPE or JAPE Plus Transducer, and point it to the _measurement\_main.jape_ file in the 'jape' folder.

Be sure to add a Tokenizer, Sentence Splitter, POS Tagger and Tagger_Numbers processing resources to your pipeline before running this plugin.
