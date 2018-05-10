Large Scale OCR Extraction, Image Captioning and Object Recognition and Enrichment of UFO Sightings Data (Team 13)

Group Members
1. Soravis Taekasem (taekasem@usc.edu)
2. Surasit Prakunhungsit (prakunhu@usc.edu)
3. Theerapat Chawannakul (tchawann@usc.edu)
4. Yifan Wu (ywu352@usc.edu)

Project Directory
- TEAM_13_ENRICHMENT.pdf - Report file
- SRC Directory - Directory contain source code
	- OCR Directory - Directory contain scripts related to OCR module
	- ExtraCredit Directory - Directory contain scripts related to extra credit portion
		- NER Directory - Contains script to perform NER on extracted description files
			- run_{method}.sh - shell scripts to iterate all extracted description files, then calls {method.sh}
			- {method}.sh - shell scripts that will execute TikaCLI using specific NER parser
		- Retraining Directory - Contains retraining models of inception_v3 and v4 and retraining scripts for inception_v3 and inception_v4 models
	- TextExtraction - Directory contain scripts related to text extraction module
	- textcleaner.sh - Fred’s ImageMagick script textcleaner plugin script used to reduce image noise
	- UfoStalkerScripts - Directory contains scripts related to scrape and retrieve images and JSON data from ufostalker.com
		- image_grabber.py - Python script to download all submitted images
		- img2caption.py - Python script to post image to img2txt server
		- img2object.py - Python script to post image to inception server
		- split_description.py - Python script to extract description of each row into separate files for NER processing
		- combine_ner.py - Python script to join all extracted entities to TSV file
	- ufo-pdf-paser.zip - An archive of our team custom Tika parser source code. This is a maven project. To compile as jar, run ‘mvn clean install’. To use it, add the jar to java classpath and then specify ‘edu.usc.irds.UFOPDFParser’ as a parser in tika-config.xml (don't forget to add --config=tika-config.xml)
- Output Directory - Directory contain output files
- v2_dataset_final.tsv - Final TSV file

External Libraries
- Fred’s ImageMagick script textcleaner
	- Run the plugin using command “sh textcleaner.sh <parameter>”
	- http://www.fmwconcepts.com/imagemagick/textcleaner/