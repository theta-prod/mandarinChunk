# mandarinChunk
separate mandarin sentences to short meaningful sentence
This process prevents word-by-word reading, which can cause lack of comprehension, 
since students forget the beginning of a sentence before they get to the end (Casteel, 1988)
Chunking is the grouping of words in a sentence into short meaningful phrases (R.4)
Chunking is a procedure of breaking up reading material into manageable sections

## Research

### tips:
1. short meaningful phrases usually three to five words (R.4)


### chunking stragegy
  - human chunking strategy: (R.2)
1. Circle the words that were unfamiliar. <KEYWORDS WEIGHT>
2. Used context clues to help define.  <POS TAGS>
3. Looked up the meaning of unknown words.  <NEW-Words WEIGHT>
4. Wrote synonyms for these new words in the text. <NEW-Words WEIGHT>
5. Underlined important places and people and identify.  <POS TAGS>
6. Read aloud. <sentence smooth>
7. Read multiple times. <sentence smooth>

- Three Types of Errors Performed in Chunking (R.1)
  - Slash placed where the text cannot be divided. <sentence smooth>
  - Slash inappropriately placed but does not hamper reading.
  - Failure to notice the phrase boundary.  <sentence format>
	
	


### Machine Vaildate Rule Plan
|  id    |  Category    |  shortname      |  bias  |  baselines                       |
| :----: | ----         | ----            | :----: | ----                             |
| 1      |  1.KEYWORDS  | Keyword         | -1     | contain a keyword                |
| 2      |  1.KEYWORDS  | Keywords Mass   | -1     | contain too many keywords        |
| 3      |  2.NEWWORDS  | NEWword         | -1     | contain a new word               |
| 4      |  2.NEWWORDS  | NEWwords Mass   | -1     | contain too many new-words       |
| 5      |  3.POS TAGS  | POS             | -1     | contain experts POS              |
| 6      |  3.POS TAGS  | POSMass         | -1     | contain too many experts POSs    |
| 7      |  3.POS TAGS  | POSHeadTail     | -1     | start or end with experts POS    | 
| 8      |  3.POS TAGS  | SentCompleted   | -1     | contain experts POS suit         | 
| 9      |  4.Sentence  | SentLength      | -1     | vaildate with length of sentencs | 

## Reference

1. [The influence of chunking on reading comprehension: Investigating the acquisition of chunking skill](https://www.researchgate.net/publication/289208481_The_influence_of_chunking_on_reading_comprehension_Investigating_the_acquisition_of_chunking_skill)
2. [THE EFFECTIVENESS OF USING CHUNKING STRATEGY TO IMPROVE STUDENTS’ READING COMPREHENSION AT THE SECOND YEAR OF SMP NEGERI 2 BAROMBONG](https://www.researchgate.net/publication/323395900_THE_EFFECTIVENESS_OF_USING_CHUNKING_STRATEGY_TO_IMPROVE_STUDENTS'_READING_COMPREHENSION_AT_THE_SECOND_YEAR_OF_SMP_NEGERI_2_BAROMBONG)
3. [jieba查找最大概率路径](https://blog.csdn.net/Claire_Mk/article/details/122031761)
4. [Chunking and Questioning Aloud Strategy Summary Sheet ] (https://nceo.umn.edu/docs/presentations/nceo-lep-iep-ascdhandoutchunking.pdf)

### CKIP POS
[test url](https://ckip.iis.sinica.edu.tw/service/corenlp/)
| Tag | CKIP Name | CKIP Description   | examples                     |
|-----|-----------|--------------------|------------------------------|
| A   | A         | 非謂形容詞         | 大陸製,唯一,綜合             |
|     | Caa       | 對等連接詞         | 或                           |
|     | Cab       | 連接詞             | 等等                         |
|     | Cba       | 連接詞             | 的話                         |
|     | Cbb       | 關聯連接詞         | 並,且,而                     |
|     | D         | 副詞               | 將要,卻,突然,不,所,有史以來  |
|     | Da        | 數量副詞           | 至少,才                      |
|     | Dfa       | 動詞前程度副詞     | 很,最,太                     |
|     | Dfb       | 動詞後程度副詞     |                              |
|     | Di        | 時態標記           | 了,起來,著                   |
|     | Dk        | 句副詞             |                              |
|     | DM        | 定量式             |                              |
|     | I         | 感嘆詞             |                              |
|     | Na        | 普通名詞           | 安樂死,體育台,總統,升空      |
|     | Nb        | 專有名詞           | 人名                         |
|     | Nc        | 地方詞             | 電視台,美國                  |
|     | Ncd       | 位置詞             | 哪裡,之中                    |
|     | Nd        | 時間詞             | 今天,明天,國慶,初期          |
|     | Nep       | 指代定詞           | 這個,那個                    |
|     | Neqa      | 數量定詞           | 全,都,半                     |
|     | Neqb      | 後置數量定詞       | 多                           |
|     | Nes       | 特指定詞           | 該,每                        |
|     | Neu       | 數詞定詞           | 20,第一                      |
|     | Nf        | 量詞               | 年,位                        |
|     | Ng        | 後置詞             | 前,後,內                     |
|  S  | Nh        | 代名詞             | 自己,他,她                   |
|  N  | Nv        | 名物化動詞         | 飛行表演                     |
|     | P         | 介詞               | 遭,針對,在,為                |
|     | T         | 語助詞             | 了,呢                        |
|     | VA        | 動作不及物動詞     | 下班,上桌,當家               |
|     | VAC       | 動作使動動詞       |                              |
|     | VB        | 動作類及物動詞     | 破案,繩之於法,頒獎           |
|     | VC        | 動作及物動詞       | 執行,封殺,提名,舉辦          |
|     | VCL       | 動作接地方賓語動詞 | 前往,進軍,來到               |
|     | VD        | 雙賓動詞           |                              |
|     | VF        | 動作謂賓動詞       | 把                           |
|     | VE        | 動作句賓動詞       | 預料,報導,查獲,質詢          |
|     | VG        | 分類動詞           | 成為                         |
| A   | VH        | 狀態不及物動詞     | 順利,特別,短,努力,忙,少,漂亮 |
|     | VHC       | 狀態使動動詞       | 辛苦,均衡,緊繃               |
|     | VI        | 狀態類及物動詞     |                              |
|     | VJ        | 狀態及物動詞       | 爆出,得罪到,發生             |
|     | VK        | 狀態句賓動詞       | 懂,感謝,肯定,希望            |
|     | VL        | 狀態謂賓動詞       | 習慣,讓                      |
|     | V_2       | 有                 | 有                           |
|     | DE        | 的/之/得/地        | 的/之/得/地                  |
|     | SHI       | 是                 | 是                           |
|     | FW        | 外文               | EMO                          |

## System Design

### Variable
``` python
## Set Varibles as Arguments to adjust score
class Weights(TypedDict):
	KeywordNone: float,
	KeywordsMass: float,
	NEWword: float,
	NEWwordMass: float,
	POS: float,
	POSMass: float,
	POSBetween: float,
	POSHead: float,
	POSTail: float,
	POSCombo: float,
	SentLength: float,

	
	
	
class Condition(TypedDict):
	KeywordMaxNum: float,
	NewwordMaxNum: float,
	StrongPosMaxNum: float,

class Env(TypedDict):
	weights: Weights
	condition: Condition

Sentence = str
KeywordsList = Dict[str, int]
POS   = str
WORD = str
ExpertPOSList = Set[POS]
POSHeadTailList = Set[POS]
ChunkPos = List[POS]
ChunkWord = List[WORD]
POSCombo = List[tuple[POS,POS]]

```
### Initail vaildate standard
```
strongPosList: ExpertPOSList = []
keywordsList: KeywordsList = {}
posCombo: POSCombo = []
posSuitList: ExpertPOSList = []
def pullKeywordsList() => KeywordsList: ...

```

### Validate
```python


### (1) vaildate by word weight 
def vaildate_Keyword(chunkWord: ChunkWord, wordlist: KeywordsList) => float: ...
	# if all word of chunkWord not in wordlist : -1 * Env.weights.KeywordNone
	# if count of chunkWord in wordlist} > Env.condition.KeywordMaxNum : -1 * Env.weights.KeywordsMass
	
### (2) vaildate by new word weight 
def vaildate_NEWword(chunkWord: ChunkWord, wordlist: KeywordsList) => float:
	# if all of chunkWord's word in the wordlist : - 1 * Env.weights.NEWword
	# if count of chunkWord not in wordlist > Env.condition.NewwordMaxNum : - 1 * Env.weights.NEWwordMass


### (3) vaildate by expert's strong pos dataset (**strong pos = important pos)
def vaildate_POS(chunkPos: list[POS], strongPosList: ExpertPOSList, posCombo: POSCombo) => float: ...
	# if all unit of chunkPos not in strongPosList : -1 * Env.weights.POS
	# if count of chunkPos in strongPosList > Env.condition.StrongPosMaxNum: -1 * Env.weights.POSMass
	# if chunkPos.head not in strongPosList: -1 * Env.weights.POSHead
	# if chunkPos.tail not in strongPosList: -1 * Env.weights.POSTail
	# if combo of posCombo not in chunkPos: -1 * Env.weights.POSCombo

### (4) vaildate by sentence status
def vaildate_SentCompleted(chunkPos: ChunkPos, posSuitList: ExpertPOSList) => float: ...
	# if length of chunkPos in wordlist < 3: -1 * Env.weights.SentLength
	# if length of chunkPos in wordlist > 5: -1 * Env.weights.SentLength
	
	
```

### DataProcess
```python

class SPack(TypedDict): 
	source: Sentence
	words: ChunkWord
	poss: ChunkPos
	prefix: str
	score: float
	
def pullSentences() => List[Sentence]: ...	

def cutSentence(source: Sentence) -> Tuple[ChunkWord, ChunkPos]: ...

def buildSPack(source: Sentence) -> SPack: ...

def calculateScore(words: ChunkWord, poss: ChunkPos)-> float: ...

def findBestSPack(SPUs: List[SPack]) -> SPack: ...

def findbestcombo(words: [str], poss: [str]) -> List[Tuple[str, float]]:
    def getScore(ts: [str], ps: [str]):
        # TODO: Calculate score with argus
        return 1.0

    def head(arr: [str], arrPos: [str], keeplabel= "", ans= [], score=0):
        # 1. build prefix from head of arr.
        # 2. build tail from arr beside head
        # 3. get score with new prefix and pos of that
        # 4. update keeplabel (**keep label is result of last turn)
        #
        # if tail is empty
        #   it's mean that should return the final combo and score (new prefix + current score)
        # if not
        #   go to next round with 
        #     1. tail (without process in this round) as the base array 
        #     2. new keeplabel (calculate score is done) as keeplabel
        #     3. new prefix + current score as base-score
        # TODO: Early Stop
        # make getscore always minus
        # build and transfer a argu as the best answer
        # if current score is lower then the best answer, stop it

        for i in range(len(arr)):
            prefix = arr[:i+1]
            prefixPoss = arrPos[:i+1]
            tail = arr[i+1:]
            tailPoss = arrPos[:i+1]
            prefixLabel = "".join(prefix)
            prefixLabelScore = getScore(prefix, prefixPoss)
            newheadlabel = f"{keeplabel}/{prefixLabel}"
            if len(tail) ==0:
                return ans + [(newheadlabel, score+prefixLabelScore)] 
            ans = head(tail, tailPoss, newheadlabel, ans, score+prefixLabelScore)
    
    return head(words,poss)[0]    
        

	
```