# Europi-Cameras-Dataset
Camera Dataset for Aspect-Based Sentiment Analysis

Europi Cameras Dataset is a dataset with reviews on digital cameras collected from amazon.com, amazon.es, and amazon.it in three languages, namely English (EN), Spanish (ES), and Italian (IT).

### Annotation Process

The following protocol was adopted in the annotation process. First, we split reviews into sentences and filtered out comparative and ironic sentences. Next, for each sentence, we annotated the aspect-level information, \ie aspect, sentiment word, polarity, aspect type (implicit, explicit, or anaphora), and attribute. See below an example of an annotated sentence from our dataset. 

```xml
<sentence id="1272">
    <text>The battery life is amazing !</text>
    <Opinions>
        <Opinion category="Battery" from="4" polarity="Positive" sentiment="amazing" target="battery life" to="16" type="explicit" />
    </Opinions>
</sentence>  
```

The first four aspect-level information were obtained from the text in sentences. The attributes came from a predefined list of attributes
commonly used in product catalogs for cameras: `Battery`, `Dimension`, `Display`, `Exposure Control`, `General`, `Lens`, `Imaging`, `Memory`, `Performance`, `Price`, `Zoom`, and `Video`.

This annotation process was performed by two different human annotators and the results were compared. In case of disagreement, the annotators discussed their perceptions until they reached a consensus.

The instances in the dataset were split into train (80\%) and test (20\%). This split was stratified by attribute so all attributes had the same train/test proportion.

#### Statistics of the Dataset
The resulting dataset contains a total of 950 reviews split into 1,952 sentences. 

|        | EN   |     | ES   |     | IT  |     |
|--------|------|-----|------|-----|-----|-----|
|        | Sent | Asp | Sent | Asp |Sent | Asp |
|Train   | 511  | 664 | 488  | 714 | 462 | 684 |
|Test    | 162  | 173 | 168  | 186 | 161 | 177 |

#### Distribution of the Aspects across Attributes
The distribution of the aspects across attributes is given table below. We can see that some attributes such as `Memory` have a low frequency. In most cases, the distribution is similar for the different languages. The few exceptions are `Exposure Control` and `Other` which are more frequent in IT.

| Attribute        | EN  | ES  | IT  |
|------------------|-----|-----|-----|
| Battery          | 22  | 27  | 23  |
| Dimension        | 52  | 56  | 47  |
| Display          | 12  | 17  | 17  |
| Exposure Control | 37  | 40  | 79  |
| Imaging          | 162 | 161 | 130 |
| Lens             | 46  | 34  | 15  |
| Memory           | 2   | 6   | 3   |
| Performance      | 15  | 15  | 26  |
| Price            | 25  | 51  | 43  |
| Video            | 25  | 36  | 23  |
| Zoom             | 14  | 54  | 60  |
| General          | 328 | 260 | 191 |
| Other            | 97  | 143 | 204 |
| TOTAL            | 837 | 900 | 861 |

## Citation

If you use our dataset, please cite the following paper:

```bibtex

```
