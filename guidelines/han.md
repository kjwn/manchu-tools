한자 입력 지침
================

* 원문과 동일하게 입력한다. 원문과 일치 여부의 판정 방법은 별도 지침으로.
* 입력하지 못하는 경우 지정된 약물을 이용한다: ■(U+25A0)

## 대표자, 정자, 이체자, 이형자

원문과 동일한 형태의 한자를 입력할 수는 없으나 작업자가 대표자/정자,
이체자/이형자 지식을 가지고 있어 정보를 추가할 수 있는 경우에는 [O:] 또는 [R:]
주석을 이용한다. O는 `orignal-form'의 첫글자로 원문에 원래 쓰여있는 형태라는
의미이다. R은 `regularization'의 첫글자로 변이형태를 표준적인 형태로
정규화하였다는 의미이다.

원문에 있는 것과 동일한 형태의 한자를 입력할 수는 없으나 그것이 `肄'의
이체자라는 것을 알고 있다면 다음과 같이 입력한다.

    旣詒我肄[O:]



### 추가정보 제공의 예

한자의 형태에 대해서  추가적인 정보를 제공할 필요가 있다면 다음과 같이 O: 뒤에
추가적인 주석을 달아준다.

    旣詒我肄[O:=肄-聿+隶]

입력자가 100% 확신하지는 못하나 추후검토를 위해 대표자(정자) 정보를 남겨놓고 싶다면
다음과 같은 형식을 이용한다.

    旣詒我■[R:肄?]


### 작업 진행에 따른 정보 갱신의 예

이체자의 처리는  입력자의 지식에 따라 달라질 수 있다. 원문에 나타난 그대로 다음과 같이 입력하는 것이 기본 원칙이다. 원문과 동일하게 입력한 경우 추가적인 정보는 필요없다.

    何其乆也

그러나 입력자가 乆자를 찾지 못하였으며 이 글자에 대한 지식이 전혀 없는
경우에는  다음과 같이 입력될 수 있다.

    何其■也

나중에 다른 작업자가 검토할 때 역시 유니코드에서 乆를 찾지는 못하였으나 이것이 久의
이체자인 것 같다고 판단하였다면 다음과 같이 정보를 추가할 수 있다.

    何其■[R:久?]也

또 다른 검토자가 `久'의 이체자임을 확정하였다면 다음과 같이 물음표를 삭제한다.

    何其■[R:久]也

또 다른 검토자가 유니코드에서  乆를 찾았다면 다음과 같이 해당 한자를 추가한다. 

    何其乆[R:久]也


## 미확인 한자

원문과 동일한 한자를 찾을 수 없으며 무엇의 이체자인지부도 모르는 경우에 해당 한자의 모양에 대한 정보를 다음과 같이 [H:] 주석을 이용하여 추가할 수 있다.

    ■[H:=寉頁]

위의 정보제공 방법에 엄밀한 형식은 없다.  유니코드에는 이러한 미등록 한자의
모양을 표현하는 규약이 마련되어있으나 복잡하므로 그것을 따르지는 않는다.


## 맹백한 오류

### 오자 교정

원문에 잘못 쓰여진 한자의 교정에는 [S:]와 [C:] 주석을 이용한다. S는 `sic'의
첫글자로 있는 그대로 옮긴다는 의미이다. C는 `correction'의 첫글자로 교정한다는
의미이다. 

원문의 오자를 있는 그대로(sic) 입력하고 교정(corr) 정보를 추가한다. 예를 들어,
원문에 鞠으로 되어있으나 鞫이 맞는 경우에 다음과 같이 입력한다.

    昔育恐育鞫[S:鞠]

원문이 틀렸는지 여부가 불확실하거나 교정에 대해 자신이 없으나 추후검토를 위해
정보를 남기고자 할 때에는 다음과 같이 입력한다.

    昔育恐育鞠[C:鞫?]

다른 작업자가 검토하여 옳은 판단이라고 확정한 경우에 물음표를 삭제한다.

    昔育恐育鞠[C:鞫]

이러한 교정 양식은 한 글자씩 적용한다. 여러 글자를 동시에 교정하지 않는다.

### 누락된 한자 추가

원문에 누락된 한자가 있을 때에는 [+:] 주석을 이용하여 추가해준다. 예를 들어, "章四句"라고 쓰여야 마땅하나 "章四"라고 쓰여있는 경우 다음과 같은 형식으로 추가해 준다.

    章四[+:句]

여러 글자를 하나의 주석으로 추가할 수 있다.

    雖以熹之不敏亦幸[+:私淑]而有與聞焉


### 과잉된 부분의 삭제

원문에 과잉된 한자가 있을 때에는 [-:] 주석을 이용하여 둘러싼다. 예를들어,
원문에 `動'가 실수로 두번 연달아 쓰여있다면 다음과 같이 과잉된 부분을 [-:]로 둘러싼다.

    一言一動[-:動]皆書之格册

여러 글자를 하나의 주석으로 뺄 수 있다.
