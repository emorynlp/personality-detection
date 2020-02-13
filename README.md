# FriendsPersona: Personality Recognition on Multiparty Dialogue

## Task description

Multiparty Personality Recognition requires machines to determine the main speaker's personality from a short conversation in binary Big Five personality traits:
  - **Agreeableness (AGR)**: trustworthy, straightforward, generous vs. unreliable, complicated, meager, and boastful
  - **Conscientiousness (CON)**: efficient and organized vs. sloppy and careless
  - **Extroversion (EXT)**:  outgoing, talkative, and energetic vs. reserved and solitary
  - **Openness (OPN)**: inventive and curious vs. dogmatic and cautious
  - **Neuroticism (NEU)**: sensitive and nervous vs. secure and confident

This is a part of the [Character Mining](../../../character-mining) project led by the [Emory NLP](http://nlp.mathcs.emory.edu) research group.

## Dataset

To generate the dataset, 711 short conversations are extracted and annotated from the first four seasons of Friends TV Show transcripts. 
There are 6405 unique tokens after pre-processing. 
In each short conversation, we ask three annotators to evaluate a main speaker's personality traits on a scale of -1, 0, 1. 
This task is challenging because only text information is given and might not contain enough information to fully understand the social context.


## Annotation

The following shows a multiparty dialogue between **Monica** and **Paul**. 

<b>s01_e01_c05(0) for Paul</b><br>
<b>Monica Geller</b>: Oh my God!<br>
<b>Paul</b>: I know, I know, I'm such an idiot. I guess I should have caught on when she started going to the dentist four and five times a week. I mean, how clean can teeth get?<br>
<b>Monica Geller</b>: My brother's going through that right now, he's such a mess. How did you get through it?<br>
<b>Paul</b>: Well, you might try accidentally breaking something valuable of hers, say her-<br>
<b>Monica Geller</b>: -leg?<br>

<div hidden="" id="template">
<div class="col-xs-12 fields">
<div class="form-group"><label class="group-label">Based on the conversation, Paul is : </label>
<table class="table table-condensed table-striped table-responsive">
	<colgroup>
		<col class="col-xs-3 col-md-3" />
		<col class="col-xs-3 col-md-3" />
		<col class="col-xs-3 col-md-3" />
		<col class="col-xs-3 col-md-3" />
	</colgroup>
	<tbody>
	    <tr>
			<th>Agreeable:&nbsp;&nbsp;</th>
			<th><input name="agreeable" type="radio" value="1" /> 1</th>
			<th><input name="agreeable" type="radio" value="0" /> 0</th>
			<th><input name="agreeable" type="radio" value="-1" /> -1</th>
		</tr>
		<tr>
			<th>Conscientious:&nbsp;&nbsp;</th>
			<th><input name="conscientious" type="radio" value="1" /> 1 </th>
			<th><input name="conscientious" type="radio" value="0" /> 0 </th>
			<th><input name="conscientious" type="radio" value="-1" /> -1 </th>
		</tr>
		<tr>
			<th>Extraverted:&nbsp;&nbsp;</th>
			<th><input name="extraverted" type="radio" value="1" /> 1</th>
			<th><input name="extraverted" type="radio" value="0" /> 0</th>
			<th><input name="extraverted" type="radio" value="-1" /> -1</th>
		</tr>
		<tr>
			<th>Open to experience:&nbsp;&nbsp;</th>
			<th><input name="open" type="radio" value="1" /> 1</th>
			<th><input name="open" type="radio" value="0" /> 0</th>
			<th><input name="open" type="radio" value="-1" /> -1</th>
		</tr>
		<tr>
			<th>Emotionally Stable:&nbsp;&nbsp;</th>
			<th><input name="stable" type="radio" value="1" /> 1</th>
			<th><input name="stable" type="radio" value="0" /> 0 </th>
			<th><input name="stable" type="radio" value="-1" /> -1 </th>
		</tr>
	</tbody>
</table>
</div>
</div>
</div>


The scores of 3 annotators are summed up and converted to binary labels using the median split.
This conversation has the following fields:
  - `scene_id`: s01_e01_c05
  - `character`: Paul
  - `AGR`: 1
  - `CON`: 0
  - `EXT`: 1
  - `OPN`: 1
  - `NEU`: 0
  - `text`: 

```html
<b>s01_e01_c05(0) for Paul</b><br><br>
<b>Monica Geller</b>: Oh my God!<br><br>
<b>Paul</b>: I know, I know, I'm such an idiot. I guess I should have caught on when she started going to the dentist four and five times a week. I mean, how clean can teeth get?<br><br>
<b>Monica Geller</b>: My brother's going through that right now, he's such a mess. How did you get through it?<br><br>
<b>Paul</b>: Well, you might try accidentally breaking something valuable of hers, say her-<br><br>
<b>Monica Geller</b>: -leg?<br><br>
```

Note: The `text` column consists conversation text strings in simple HTML format. 
  Each text starts with its scene id (e.g. s01_e01_c05) and the main speaker (e.g. Paul).
  Each utterance is separated by `<br><br>` and each speaker is highlighted with `<br></br>`.


## Citation

* [Automatic Text-based Personality Recognition on Monologues and Multiparty Dialogues Using Attentive Networks and Contextual Embeddings](https://arxiv.org/abs/1911.09304). [Hang Jiang](https://hjian42.github.io/), Xianzhe Zhang, and Jinho D. Choi. ([pdf](https://arxiv.org/abs/1911.09304); [poster](https://hjian42.github.io/files/aaai2020-poster.pdf); [slide](https://hjian42.github.io/files/435_Jiang.pdf))

## Contact

* [Jinho D. Choi](http://www.mathcs.emory.edu/~choi).




