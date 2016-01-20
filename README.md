1. 代码下载:http://word2vec.googlecode.com/svn/trunk/

2. 首先运行"make"编译word2vec工具。

3. 运行demo脚本：./demo-word.sh
   demo-word.sh的主要工作为：
   1）编译（make）
   2）下载训练数据text8（text8 中为一些空格隔开的英文单词,但不含标点符号,一共有 1600 多万个单词。）
   3）训练
   4）调用distance，查找最近的词
训练完毕后,输入 china 就会找出与其最相近的词:
Enter word or sentence (EXIT to break): china


ord: china  Position in vocabulary: 486

                                              Word       Cosine distance
------------------------------------------------------------------------
                                            taiwan		0.631476
                                             japan		0.628714
                                            hainan		0.574206
                                             tibet		0.571605
                                          kalmykia		0.570422
                                            xiamen		0.557087
                                               prc		0.554758
                                         manchuria		0.550517
                                             wuhan		0.549730
                                           chinese		0.546243
                                             hubei		0.542150
                                              tuva		0.541253
                                             india		0.538744
                                             korea		0.537304
                                             hunan		0.529424
                                         chongqing		0.529336
                                              liao		0.529142
                                          hangzhou		0.528957
                                            ......
可以看到台湾出现在第一行

4. 也可以自己执行其他相关的程序,比如向量加减法操作,在命令行执行./word-analogy vectors.bin
wang@wang-H87-D3H:~/learngit/word2vec-master$ ./word-analogy vectors.bin
Enter three words (EXIT to break): france paris china

Word: france  Position in vocabulary: 303

Word: paris  Position in vocabulary: 1055

Word: china  Position in vocabulary: 486

                                              Word              Distance
------------------------------------------------------------------------
                                            peking		0.541911
                                           beijing		0.529382
                                          shanghai		0.521304
                                             guang		0.490429
                                           nanjing		0.466513
                                               liu		0.462037
                                            zedong		0.456045
                                             jiang		0.453668
                                          hangzhou		0.453322
                                           chinese		0.452750
                                         chongqing		0.441029
                                            moscow		0.439971
                                             hunan		0.434052
                                          shenzhen		0.431259
                                             zhang		0.431177
                                           chengdu		0.429605
                                             liang		0.427251
                                               mao		0.426958
                                              deng		0.425877
                                            hainan		0.424533
                                             zheng		0.423342
                                       bodhidharma		0.422031
                                            taipei		0.420125
                                            chiang		0.417210
                                              xuan		0.415464
                                              zhou		0.413037
                                              ziyi		0.412160
                                           luoyang		0.410887
                                              ming		0.410557
                                              kobe		0.409661
                                             hubei		0.408253
                                             chang		0.404251
                                               cai		0.404033
                                              fung		0.402991
                                               jia		0.401088
                                              tian		0.400376
                                               jin		0.397778
                                              shih		0.397590
                                        kuomintang		0.395071
                                             wuhan		0.394555
可以看到北京的旧称peking出现在第一行


