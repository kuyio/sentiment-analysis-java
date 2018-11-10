# sentiment-analysis-java

Example implementation of AFINN and SentiNet 3.0 sentiment analysis.

## Usage

- Build with gradle.
- Run the `App` main file with passing in a string to obtain AFINN and SentiNet3 scores.

## Example

Calculate sentiment for a fictitious product review:

```sh
./gradlew run --args="'The product works really well. Does it exaclty what it says, well worth the price. Quality could be better.'"

> Task :run
AFINN SCORE: 4
SWN SCORE: 0.21629727936297283

BUILD SUCCESSFUL in 1s
2 actionable tasks: 1 executed, 1 up-to-date
```

## AFINN

Implements AFINN-111.

AFINN is a list of English words rated for valence with an integer
between minus five (negative) and plus five (positive). The words have
been manually labeled by Finn Årup Nielsen in 2009-2011. The file
is tab-separated. There are two versions:

AFINN-111: Newest version with 2477 words and phrases.

## SentiNet 3.0

Sentiment scores are between -1 and 1, greater than 0 for positive and less than 0 for negative.

Dictionary-based sentiment analysis does not perform as well as a trained classifier, but it is domain-independent, based on a priori knowledge of words' sentiment values.

The class handles negations and multiword expressions.

## Credits

AFINN: http://www2.imm.dtu.dk/pubdb/views/publication_details.php?id=6010
SentiNet 3.0: http://nmis.isti.cnr.it/sebastiani/Publications/LREC10.pdf