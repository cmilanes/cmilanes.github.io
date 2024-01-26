---
layout: essay
type: essay
title: "Smart Questions, Smarter Answers"
# All dates must be YYYY-MM-DD format!
date: 2024-01-25
published: true
labels:
  - Programming
  - StackOverflow
---

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions.jpg">

## What’s a smart question?
Effective communication is one of the most fundamental skills imperative for software engineers to learn. Furthermore, the art of posing 'intelligent' or ‘good’ questions is a cornerstone of professional communication. 

Broadly, a ‘smart’ question contains thorough consideration, is informative, and aims to extract some specific information. In the realm of software engineering, where questions are predominantly posed on platforms like StackOverflow, the aforementioned principles hold true along with some nuances due to the nature of online platforms.

First and foremost, a carefully constructed and informative title will increase the visibility and interaction of a post. In the content, it is essential to describe the issue clearly while also outlining the intended goal. Specifically with programming questions, including buggy or incorrect code accompanied by a detailed explanation of its intended output is very important. Implementing this method increases the probability of getting responses and also assists others who may confront similar issues.

In the following example, taken from StackOverflow, is a question pertaining to using a structure in C to get the current time and compare it to a previous date.

```
Q: How to Obtain a Time in C using a Struct

I have an issue in my C project which involves an assortment of schedules, and each schedule needs a date. I obtain it using a struct. Now I would like to delete all the old schedules, so in order to do this the code nees to:

Get the present time
Run my list to compare whether (Date(now) > Date(old)). If true, the code will delete the pertinent schedule.
The primary issue concerns how to get the real time, and pass it to my struct. Can anyone help in this regard?

The code that attempts to get the real time and put into a struct is as follows:

#include <stdio.h>
#include <time.h>

typedef struct date Date;
typedef struct hour Hour;

struct hour{

    int hour;
    int minute;
    int second;

};

struct date{

    int day;
    int month;
    int year;
    Hour hour;

};

int main (void) {

    Date date;

    //char buff[100];
    time_t now = time(0);    
    strftime (date, 100, "%d-%m-%Y %H:%M:%S", localtime(&now));
    printf ("%s\n", date);

    //I want to put localtime(&now) on date instead buff that is a char!
    //To me compare after

    return 0;

}
```
The heading of this post is very straightforward and to the point to help the reader understand what the original poster needed to be answered. This title ‘C - How to Obtain a Time in C using a Struct’ is very similar to one someone would plug into their search engine, looking for answers. This post also provided a code snippet of an attempt and provided a comment about what was confusing to the original poster, so it is easier for a response to be created.

```
A: Use struct tm together with localtime to get the individual values for day, month, year, and so on. 

Then you can either copy the values to your own struct, or you can use struct tm directly and throughout in your code. Note that - when copying to your struct - some values need to be adapted if you want to have, for example, 2017 as a years value instead of 117:

int main (void) {

    Date date;

    char buff[100];
    time_t now = time(0);
    struct tm now_t = *localtime(&now);
    strftime (buff, 100, "%d-%m-%Y %H:%M:%S", &now_t);

    date.year = now_t.tm_year + 1900; // years since 1900
    date.month = now_t.tm_mon + 1;  // months since January [0-11]
    date.day = now_t.tm_mday;  // day of month [1-31]

    date.hour.hour = now_t.tm_hour;
    date.hour.minute = now_t.tm_min;
    date.hour.second = now_t.tm_sec;

    return 0;
}

```

The asker received two possible answers, with some discussion from multiple users. The answers were clear and provided some good examples about how to layout the code and some comments about things to note. 

## Conclusion

Looking for assistance from others' generosity and expertise on online forums is very useful. It's important that questions are created to get efficient and effective help, which would benefit both the inquirer and those who provide answers, along with those that may have potential future questions. Therefore, it's crucial to ensure that each question is thoughtful and strategic. While asking questions doesn't always guarantee the best answer, framing them in a manner that would encourage engagement and follow up posts will increase the likelihood of finding a satisfactory solution
