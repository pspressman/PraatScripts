# PraatScripts
Some simple Praat scripts I've written or modified, often with assistance by others such as JJ Atria, in order to analyze dyadic interactions after speakers and noise are labeled in Praat. 

To understand the use of these scripts, some background is needed.  These are designed to run over conversations between two people.  Manual labeling is done for speech and non-speech sounds throughout.  Speaker 1 (whomever speaks first) is in Tier 1, Speaker 2 is in Tier 2, nonspeech sounds attributed to Speaker 1 go in Tier 3,  nonspeech sounds attributed to Speaker 2 in Tier 4.  Speech is labeled <sp>.  Noise-- nonspeech sounds and non-utterances are attributed to neither speaker, is labeled <noise>, and can go in either Tier 3 and Tier 4.  All tiers are then "flattened" into one tier that defines oral utterances for each speaker, which does not overlap with any non-speech sound or noise. 

Many scripts are VERY closely adapted from Celine DeLooze and/or JJ Atria, who should be appropriately recognized.  Almost all scripts are designed to loop through a folder containing identically named wav files and TextGrids formatted as above. 

Note that I've tinkered in Praat for a long time, so the syntax may be dated. 

layerflattener: this is used to ensure that the four tiers are "flattened" as described into one for future analysis. 
syl_counter: this actually does more than syllable counting, but also gives good measures of speech rates and more.  The syllable counter is adapted from DeJong et al 2009-ish. 
get -pitch-w-semitone: this is a script that gets pitch measures throughout the conversation  for each speaker. 
depausifier-- many original textgrids allowed a lot of variation in when borders were put down by the manual labelers, allowing for different borders for pauses.  This script merges all pauses (when one speaker stops, then starts again), into one long section to be extracted. 
ExactIntF0by DeciSec-- this loops through files and extracts measures every Decisecond, useful for finegrained analyses of how measures changes over time rather than across the whole conversation. 
GetF0perInt-- this looks at pitch measures for each interval of speech between floor exchanges. 
getlabelinfo-- this quickly extracts the written label information across all tiers for each conversation. 
