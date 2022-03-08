---
layout: feature
title: 'Aspect'
shortdef: 'aspect'
udver: '2'
---

<table class="typeindex" border="1">
<tr>
  <td style="background-color:cornflowerblue;color:white"><strong>Values:</strong> </td>
  <td><a href="#Hab">Hab</a></td>
  <td><a href="#Imp">Imp</a></td>
  <td><a href="#Iter">Iter</a></td>
  <td><a href="#Perf">Perf</a></td>
  <td><a href="#Prog">Prog</a></td>
  <td><a href="#Prosp">Prosp</a></td>
</tr>
</table>

典型的に，アスペクト (aspect) は [動詞 (verbs)](u-pos/VERB) についての特性である．動名詞 (gerund) や分詞 (participle) といった境界的な語をどのように分類するかによって，他の品詞 ([名詞 (nouns)](u-pos/NOUN), [形容詞 (adjectives)](u-pos/ADJ), [副詞 (adverbs)](u-pos/ADV)) であってもアスペクトを担うことがある．

アスペクトは行為における時間軸上の幅を指定するものであり，当該行為が完了した (completed) かどうかなどを決定する. [時制 (tenses)](Tense) について，実際には時制とアスペクトの組み合わせであるような言語 (e.g. 英語) もあれば，完全に独立はしていないものの，アスペクトと時制が分離しているような言語 (e.g. チェコ語) もある．

チェコ語や他のスラブ諸語において，アスペクトは語彙の特性である．不完了体 (imperfective) と完了体 (perfective) から成る動詞のペアが存在し，2つは形態論からみて関連はするものの，違いの規則性を見出すことが難しい．よって，動詞の2つの体は別個の見出し語 (lemma) として扱われる．

UDはボトムアップ的に記述を進めるため，現行の基準ではコーパスから確認された数点の値 (value) のみをカバーしている．他のアスペクトに関する膨大なリストについては，Wikipedia (<http://en.wikipedia.org/wiki/Grammatical_aspect>) を参照されたい．

### <a name="Imp">`Imp`</a>: 不完了体

当該行為が一定の時間幅をとった/とる/とるだろう という情報を示し，その行為がいつ完了した/完了するだろうか という情報は表さない．

#### 例

* [cs] _péci_ "to bake" (Imp); _<b>pekl</b> chleba_ "he baked / was
  baking a bread"

### <a name="Perf">`Perf`</a>: 完了体

当該行為が完了している/ 完了するだろう という情報を示す．時間軸上の一点 (完了時点) を強調するので，このアスペクトは現在時制と相性が悪い．例えば，チェコ語では完了体動詞の現在形を形態的にはつくれるが，実際は未来の意味を表す．

#### 例

* [cs] _upéci_ "to bake" (Perf); _<b>upekl</b> chleba_ "he baked / has
  baked a bread"

### <a name="Prosp">`Prosp`</a>: 前望アスペクト (prospective aspect)

一般的に，前望アスペクト (prospective aspect) は相対的な未来として記述可能である:
当該行為が，特定の時点に続いて起きる/起きた/起きるだろうと期待される; 特定の時点 (参照点) は過去，現在もしくは未来のいずれかである．
英語の文，_When I got home yesterday, John called and said he would arrive soon_において，最後尾の節 _(he would arrive soon)_ は前望アスペクトを表す．
とはいえ，英語は前望アスペクト専用の接辞を持たないので，これを標示するラベルは英語には不要である．他の言語では必要となる; バスク語の接尾辞_-ko_が例である．

前望アスペクトを標示する値は，UDv1においては`Pro`だったが，UDv2においては`Prosp`へと名称が変更されている．

#### 例

* [eu] _Liburua <b>irakurriko</b> behar du._ lit. _book-a read-Prosp must AUX_ "He must go to read a book."

### <a name="Prog">`Prog`</a>: 進行アスペクト (progressive aspect)

英語の進行時制 (_I am eating, I have been doing &hellip;_) は進行アスペクトを持つ．進行時制は分析的に構成される (助動詞+現在分詞) が，_-ing_分詞は進行の意味との結びつきが強いため，これは`Prog`として標示する方が適しているように思われる (過去分詞 (past participle) との区別が必要であるため，"時制"と"アスペクト"の素性両方を用いる)．

英語以外の言語において，進行の意味が主動詞に付加する拘束形態素によって表される場合があり，このことは`Prog`の正当性を支持する．例に挙げるのは，進行を表す2つの異なった形態素_-yor_と_-mekte_を有するトルコ語である．

#### 例


### <a name="Hab">`Hab`</a>: 習慣アスペクト (habitual aspect)

英語の単純現在時制は，このアスペクトを持つ．

### <a name="Iter">`Iter`</a>: 反復アスペクト (iterative / frequentative aspect)

反復アスペクトは繰り返される行為を示し，ハンガリー語などで観察される．
チェコ語にも反復アスペクトと呼ばれるものがあるが，どちらかといえば習慣の意味に近い．
それらは不完了体動詞のみから形成され，通常は独立したアスペクトとして分類されることがない; 単に`Aspect=Imp`として標示される．

注意点: この値はUDv2が初出である．ただし，UDv1ではこれに類似したものがハンガリー語に対して使用されていて，それを_frequentative_ (`Freq`) と呼称していた．

#### 例

* [hu] _üt_ “hit”, _<b>ütöget</b>_ “hit several times”
