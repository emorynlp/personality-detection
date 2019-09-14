# Automatic Personality Recognition on Multiparty Dialogue

Multiparty Personality Recognition requires machines to determine one main speaker's personality from a short conversation in binary Big Five personality traits:
  - **Agreeableness (AGR)**: trustworthy, straightforward, generous versus unreliable, complicated, meager, and boastful
  - **Conscientiousness (CON)**: efficient and organized versus sloppy and careless
  - **Extroversion (EXT)**:  outgoing, talk- ative, and energetic versus reserved and solitary
  - **Openness (OPN)**: inventive and curious versus dogmatic and cautious
  - **Neuroticism (NEU)**: sensitive and nervous versus secure and confident

This is a part of the [Character Mining](../../../character-mining) project led by the [Emory NLP](http://nlp.mathcs.emory.edu) research group.
The following shows a multiparty dialogue between Monica and Paul. 

## Dataset

## Format
A sample conversation has the following fields:
  - `scene_id`: 01_e01_c01
  - `character`: Joey Tribbiani
  - `AGR`: 1
  - `CON`: 0 
  - `EXT`: 1  
  - `OPN`: 1  
  - `NEU`: 0
  - `text`: `<b>s01_e01_c05(0) for Paul</b><br><br><b>Monica Geller</b>: Oh my God!<br><br><b>Paul</b>: I know, I know, I'm such an idiot. I guess I should have caught on when she started going to the dentist four and five times a week. I mean, how clean can teeth get?<br><br><b>Monica Geller</b>: My brother's going through that right now, he's such a mess. How did you get through it?<br><br><b>Paul</b>: Well, you might try accidentally breaking something valuable of hers, say her-<br><br><b>Monica Geller</b>: -leg?<br><br>
`

## Demo 
The `text` column consists of the original HTML files used for each conversation to annotate. 

<b>s01_e01_c05(0) for Paul</b><br><br><b>Monica Geller</b>: Oh my God!<br><br><b>Paul</b>: I know, I know, I'm such an idiot. I guess I should have caught on when she started going to the dentist four and five times a week. I mean, how clean can teeth get?<br><br><b>Monica Geller</b>: My brother's going through that right now, he's such a mess. How did you get through it?<br><br><b>Paul</b>: Well, you might try accidentally breaking something valuable of hers, say her-<br><br><b>Monica Geller</b>: -leg?<br><br>
`

