# mandarinChunk
separate mandarin sentences to short meaningful sentence
This process prevents word-by-word reading, which can cause lack of comprehension, 
since students forget the beginning of a sentence before they get to the end (Casteel, 1988)
Chunking is the grouping of words in a sentence into short meaningful phrases (R.4)
Chunking is a procedure of breaking up reading material into manageable sections


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
|  id    |  Category    |  shortname      |  bias |  baselines                       |
| :----: | ----         | ----            | :----:| ----                             |
| 1      |  1.KEYWORDS  | Keyword         | +     | contain a keyword                |
| 2      |  1.KEYWORDS  | Keywords Mass   | -     | contain too many keywords        |
| 3      |  2.NEWWORDS  | NEWword         | +     | contain a new word               |
| 4      |  2.NEWWORDS  | NEWwords Mass   | -     | contain too many new-words       |
| 5      |  3.POS TAGS  | POS             | +     | contain experts POS              |
| 6      |  3.POS TAGS  | POSMass         | -     | contain too many experts POSs    |
| 7      |  3.POS TAGS  | POSBetween      | +     | Between two POS                  |
| 8      |  3.POS TAGS  | POSHeadTail     | +     | start or end with experts POS    | 
| 9      |  4.Sentence  | SentCompleted   | +     | contain experts POS suit         | 
| 10     |  4.Sentence  | SentLength      | +     | vaildate with length of sentencs | 

### Reference

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

### Code Design

``` python
class Weights(TypedDict):
	Keyword: float,
	KeywordsMass: float,
	NEWword: float,
	NEWwordMass: float,
	POS: float,
	POSMass: float,
	POSBetween: float,
	POSHead: float,
	POSTail: float,
	SentLength: float,
	SentCompleted: float,

class Env(TypedDict):
	weights: Weights
	
	
KeywordsList = NewType("KeywordsList", Dict[str, int])

def pullKeywordsList() => KeywordsList:
	pass

### (1)
def vaildate_Keyword(chunkContent: str, wordlist: KeywordsList) => float:
	# if chunkContent in wordlist : +{...} * Env.weights.Keyword
	# else: +0

def vaildate_KeywordsMass(chunkContent: str, wordlist: KeywordsList) => float:
	# if count of chunkContent in wordlist} > {1}: -{...} * Env.weights.KeywordsMass
	# else: -0
	
### (2)
def vaildate_NEWword(chunkContent: str, wordlist: KeywordsList) => float:
	# if chunkContent not in wordlist : +{...} * Env.weights.NEWword
	# else: +0

def vaildate_NEWwordsMass(chunkContent: str, wordlist: KeywordsList) => float:
	# if count of chunkContent not in wordlist} > {1}: -{...} * Env.weights.NEWwordMass
	# else: -0



### (3)
POS   = NewType("POS", str)
POSList = NewType("POSList", Set[POS])
POSHeadTailList = NewType("POSHeadTailList", Set[POS])
POSConnectSuitList = NewType("POSConnectSuitList", List[tuple[POS,POS]])
ChunkPos = NewType("ChunkPos", List[POS]) 

def vaildate_POS(chunkPos: list[POS], posList: POSList) => float:
	# if chunkPos in posList : +{...} * Env.weights.POS
	# else: +0

def vaildate_POSMass(chunkPos: list[POS], posList: POSList) => float:
	# if count of chunkPos in posList} > {1}: -{...} * Env.weights.POSMass
	# else: -0

def vaildate_POSBetween(chunkPos: ChunkPos, beforeChunkPos: ChunkPos, posSuitList: POSConnectSuitList) => float:
	# if (beforeChunkPos.tail, chunkPos.head) in posSuitList: +{...} * Env.weights.POSBetween
	# else: +0
	
def vaildate_POSHeadTail(chunkPos: ChunkPos, posHeadTailList: POSHeadTailList) => float:
	# if chunkPos.head in posHeadTailList: +{...} * Env.weights.POSHead
	# else: +0
	# if chunkPos.tail in posHeadTailList: +{...} * Env.weights.POSTail
	# else: +0



### (4)
POSContainSuit = NewType("POSContainSuit", Set[POS,POS])
POSContainSuitPoint = NewType("POSContainSuitPoint", int)
POSContainSuitList = NewType("POSContainSuitList", List[tuple[POSContainSuit,POSContainSuitPoint]])

def vaildate_SentCompleted(chunkPos: ChunkPos, posSuitList: POSContainSuitList) => float:
	# if element of posSuitList.POSContainSuit in chunkPos : 
	#	+{posSuitList.POSContainSuitPoint} * Env.weights.SentCompleted
	# else: +0

def vaildate_SentLength(chunkContent: str) => float:
	# if 5 > length of chunkContent in wordlist} > 3: +{...} * Env.weights.SentLength
	# else: +0
```