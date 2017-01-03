---
title: "Math"
layout: page
date: 2016-12-5 19:41
---

[TOC]

<script type="text/javascript"
   src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

# 《数学之美》读书笔记 #

## chapter 1 ##

文字、数字、语言之间的天然关系

little knowlege: 

- 罗塞塔石碑

- 圣经的抄写。希伯来文字代表数字，每行加起来得到一个校验码。

## chapter 2 ##

自然语言处理：语言相当于一次编码过程，人的理解相当于解码。而机器的自然语言理解，在发展初期，认为应该和人具有一样的理解方式。文法分析树的生成过于复杂，需要理解的情况过于庞大。特别是
上下文相关的情况，计算复杂度基本上是语句长度的六次方。而统计语言学，最初应用于语音识别，的出现改变了这一状况。

这个过程中，比较有趣的是，语法分析到统计方法的转变花了十多年的时间，等待原有的一批语言学家退休。而处在那个时期，也的确不好判断发展方向，一方面，句法分析已经经过了长时间的发展，而随着
计算能力的发展，有可能通过这种复杂的方法，精确地通过文法树翻译出来。而统计学方法，由于当时的计算能力，以及统计数据库大小的限制，至少在机器翻译领域，并没有很好的表现。另外，自然语言
处理的应用也随着其它领域的崛起，发生了变化。自动问答需求被网页搜索数据挖掘取代，而应用到机器翻译，语音识别等领域。

## chapter 3 ##

统计语言模型(Staticstical Language Model)是今天所有自然语言处理的基础。 广泛应用于机器翻译，语音识别，印刷体和手写体识别，拼写纠错，汉字输入和文献查询。

出发点：一个句子是否合理，就看它的可能性大小如何。

假设S表示一个句子，由\\(w\_{1},w\_{2},...,w\_{n}\\)组成。通常，N元模型：

P(S)
= <img src="http://chart.googleapis.com/chart?cht=tx&chl= P\left(w_{1},w_{2},...,w_{n}\right)" style="border:none;">
= <img src="http://chart.googleapis.com/chart?cht=tx&chl= P\left( W_{1}\right) \cdot P\left( W_{2}|W_{1}\right) \cdot P\left( W_{3}|W_{1},W_{2}\right) \cdot \cdot P\left( W_{n}|W_{1},W_{2},\ldots ,W_{n-1}\right)" style="border:none;">

简化，马尔可夫假设，二元模型（bigram model）


<img src="http://chart.googleapis.com/chart?cht=tx&chl=P\left(S\right)=P\left( W_{1}\right) \cdot P\left( W_{2}|W_{1}\right) \cdot P\left( W_{3}|W_{2}\right) \ldots P\left( W_{n}|W_{n-1}\right)" style="border:none;">

结果计算取决于语料库(corpus)

实际上一般采用N=3的三元模型，因为复杂度\\(O\left( \left| V\right| ^{N}\right)\\)，V为语言词库的词汇量。当模型从3到4时，效果提升不明显，但是资源耗费大。google的罗塞塔系统用的是4元模型。

限制：长程的依赖性。上下文相关跨度大。

对于小概率事件的训练，可以采用古德-图灵估计,折扣小部分概率给未看见的事件。

对于出现r次的词语：

$$r=d\_{r}=\left( r+1\right) \cdot N\_{r+1} / N\_{r} $$

对于语料的选取，训练数据最好与实际应用相符。而且，大量的易处理噪声可以预处理。

Q:
- 是否由分词的不同方式组成句子，然后比较可能性？

- 如何分割词语？


