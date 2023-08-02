# Bioinfo1_jwb
Project Works for classroom : "Bio-infomatics and practice 1" in Seoul Nat'l Univ.   


![image](https://github.com/WoobeenJeong/bioinfo1_jwb/assets/132027211/f236af06-d444-4286-98f0-815830d66478)


<span style="color:blue"> 파란 밑줄 </span>
로 된 링크를 따라, 해당 미션을 확인 가능합니다.


## Free Expansion: LIN28A RNA-seq data (날짜 : 최초작성일 기준 / 주기적 수정 존재)
* 2023-05-23
  > 주제 선정 시작 : 후보군
    - Relative frequency of Watson-Crick pair
    - Binding predictor using ML

**최종 발표 활용 작성 파일**

* 2023-06-07
 
   [> Project 005:](https://github.com/WoobeenJeong/bioinfo1_jwb/blob/main/Project_005.ipynb)
   [file name] Project_005.ipynb  
   [> Project 006:](https://github.com/WoobeenJeong/bioinfo1_jwb/blob/main/Project_006.ipynb)
   [file name] Project_006.ipynb

  > Project 005  
  1. samtools를 통해 bam을 전처리 완벽히 수행
  2. shannon entropy를 직접 구하는 식 작성 
      (for문으로 너무 어렵게 A,T,G,C를 각각 구해서 용량 크면 힘듦)
      (원리를 이해하고 작성이 가능하다는 것에 의의)
      (결과값이 맞는지 scipy.stats 패키지의 entropy와 비교)
  4. threshold를 비교해가며, shannon pick를 구상
  5. 원하는 region유도과정 확인  
  
  
  > Project 006  
  1. bam에서 나온 결과를 바탕으로 원하는 fasta sequence를 구하기
  2. 나중에 해석 시, position이 버젼때문에 달라진 점 설명 (그래도 얼추)
  3. weblogo 만들어주는 툴 사용 (참조 홈페이지 링크 게시)
  4. co-occurence가 무엇인지 공부 및 예시
  5. 개념을 최대한 적용해서 작성 (plot이 문제 많지만....)

_______________________________________________

* 2023-05-24
   
   [> Initial:](https://github.com/WoobeenJeong/bioinfo1_jwb/blob/main/initial.ipynb)
   [file name] initial.ipynb
  > initial.ipynb 작성
    - 기본 환경 세팅 및 download 파일 확인
    - Anaconda3 실행 상 문제 확인

* 2023-05-30
   
   [> Project 001:](https://github.com/WoobeenJeong/bioinfo1_jwb/blob/main/Project_001.ipynb)
   [file name] Project_001.ipynb
  > Projcect_001.ipynb 작성
    - Bioconda문제로 인해 Colab에서 작성 일단 진행 
    - RAM 사용량 이슈로 인해 프로젝트를 나누어서 분할 진행
    - Shannon entrophy 바탕으로 다양한 형태의 trial

* 2023-05-31

   [> Project 002:](https://github.com/WoobeenJeong/bioinfo1_jwb/blob/main/Project_002.ipynb)
   [file name] Project_002.ipynb
  > Projcect_002.ipynb 작성
    1) C=Shannon’s entrophy를 CRES: Crosslinking-induced reverse transcription error score로 가져감  
    2) 이때, insertion은 무시 substitution과 deletion고려  
    3) Read는 rRNA,tRNA,adapte제외하고 GSNAP의 Refseq에 align  
    4) 이를 바탕으로, 먼저 CRES(0.8) 상 depth  50 reads 이상

* 2023-06-04

   [> Project 003:](https://github.com/WoobeenJeong/bioinfo1_jwb/blob/main/Project_003.ipynb)
   [file name] Project_003.ipynb
  > Projcect_003.ipynb 작성
    - 타깃 chr9에 대해 mirlet7g motif분석
    - 결과상으로는 LARS2 ptn coding region motif가 나옴
    - 버전이 서로 달라서 그런 것으로 확인

* 2023-06-05

   [> Project 004:](https://github.com/WoobeenJeong/bioinfo1_jwb/blob/main/Project_004.ipynb)
   [file name] Project_004.ipynb  
   [> Project 004_5:](https://github.com/WoobeenJeong/bioinfo1_jwb/blob/main/Project_004_5.ipynb)
   [file name] Project_004_5.ipynb
   
  > Projcect_004.ipynb 작성 + 4.5도 작성
    - 해당 region구해서 결과물 작성
    - motif추정 구역 -6,+6까지 확인
    - normalization과 bit score 둘 다 wordlogo 작성
    참조 사이트 : https://github.com/jbkinney/logomaker/tree/master/logomaker/tutorials
    - 다양한 형태로 작성하는 법 알려주며, 간단한 예시도 존재하므로 활용 용이
    - 여기서도 information이라는 함수를 바탕으로 shannon entropy를 고려

 
_______________________________________________




## Contents: LIN28A RNA interaction
* 2023-04-28 **[ Mission 1 ]**
  > what and why does it bind
  
  > RNA-seq의 applied version인 Ribosome seq과 CLIP-seq 결과물을 바탕으로 *Lin28a* knockdown한 cell에서 두 관측결과의 상관관계를 파악한다. 핵심 역량은 1)Ribo-seq과 CLIP-seq의 이해 2)Normalization 3)Cutoff설정

  <p align="left">
  <img src="https://github.com/WoobeenJeong/bioinfo1_jwb/assets/132027211/7ca151d3-76b6-4f95-aecd-c722d0416f04" alt="image" width="auto" height="100">
  </p>

   [> Mission 1:](https://github.com/WoobeenJeong/bioinfo1_jwb/blob/main/CoLab_TermProj_2023_1.ipynb)
   [file name] CoLab_TermProj_2023_1.ipynb
 
  <p align="left">
  <img src="https://github.com/WoobeenJeong/bioinfo1_jwb/assets/132027211/76811af1-eac4-4fc0-b506-7267fd12e05e" alt="image" width="auto" height="100">
  </p>
   
   [> Not a Mission 1.5:](https://github.com/WoobeenJeong/bioinfo1_jwb/blob/main/CoLab_TermProj_2023_1_5.ipynb)
   [file name] CoLab_TermProj_2023_1_5.ipynb

* 2023-05-05 **[ Mission 2 ]**
  > Ribosomal footprint density near start and stop codons
  
  > Translation region을 확인하는 Ribosome-seq을 바탕으로 start와 stop가까이에 얼마나 많은 read가 align되었는지를 파악한다. 특히 3 nucleotide단위로 읽기때문에 첫 peak가 높고 이후로 줄어드는 그림의 특징을 인지한다. 
 
  <p align="left">
  <img src="https://github.com/WoobeenJeong/bioinfo1_jwb/assets/132027211/cb6520ea-825e-4c50-96fd-2c9de0f7a3df" alt="image" width="auto" height="100">
   </p>
  
   [> Mission 2:](https://github.com/WoobeenJeong/bioinfo1_jwb/blob/main/CoLab_TermProj_2023_2.ipynb)
   [file name] CoLab_TermProj_2023_2.ipynb

* 2023-05-12 **[ Mission 3 ]**
  > Error accumulated near the binding site
  
  > Binding site주변에는 많은 biological 및 mechanical error가 발생할 수 있다. 이때, 정보량을 바탕으로 shannon index를 구함으로써 해당 위치에서의 변이를 관찰할 수 있다.
  
   <p align="left">
  <img src="https://github.com/WoobeenJeong/bioinfo1_jwb/assets/132027211/fa606df3-c84c-4c16-9844-72dab6d55a55" alt="image" width="auto" height="100">
   </p>

   [> Mission 3:](https://github.com/WoobeenJeong/bioinfo1_jwb/blob/main/CoLab_TermProj_2023_3.ipynb)
   [file name] CoLab_TermProj_2023_3.ipynb

