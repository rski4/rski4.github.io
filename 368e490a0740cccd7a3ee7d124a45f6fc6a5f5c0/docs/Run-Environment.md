---
title: "Coe Baseball Analytics Run Tables"
author: "Ryan Baranowski"
date: "8/29/2019"
output: 
  html_document:
    self_contained: false
    keep_md: true
---





# Run Environment

This report studies the run environment for the American Rivers Conference (ARC), formerly the Iowa Intercollegiate Athletic Conference (IIAC). A run environment describes how many, and how frequently, runs are scored during ARC games and can be used to make informed decisions regarding in-game strategy and player development. The run environment information is created using game data from ARC games.

## Data

The data used are game boxscores from 2002-2019 and play by play data from 2017-2019 all collected through the ARC website. Game include all games played by ARC school members.

## Basics

Using game boxscore data from 2002-2019 we can look at run scoring in the ARC. Over the last five years, home teams have averaged about 5.5 runs per game while away teams are averaging closer to 6 runs per game. In any given inning, home teams average about 0.68 runs and away teams average around 0.7 runs.  
<table class="table table-striped table-hover" style="font-size: 12px; margin-left: auto; margin-right: auto;">
<caption style="font-size: initial !important;">Runs Per Game</caption>
 <thead>
<tr>
<th style="border-bottom:hidden" colspan="1"></th>
<th style="border-bottom:hidden; padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; " colspan="2"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Home</div></th>
<th style="border-bottom:hidden; padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; " colspan="2"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Away</div></th>
<th style="border-bottom:hidden" colspan="1"></th>
</tr>
  <tr>
   <th style="text-align:center;"> Year </th>
   <th style="text-align:center;"> Runs </th>
   <th style="text-align:center;"> R/Inning </th>
   <th style="text-align:center;"> Runs </th>
   <th style="text-align:center;"> R/Inn </th>
   <th style="text-align:center;"> Innings </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 2002 </td>
   <td style="text-align:center;"> 6.25 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 6.27 </td>
   <td style="text-align:center;"> 0.86 </td>
   <td style="text-align:center;"> 7.26 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2003 </td>
   <td style="text-align:center;"> 6.17 </td>
   <td style="text-align:center;"> 0.84 </td>
   <td style="text-align:center;"> 6.05 </td>
   <td style="text-align:center;"> 0.83 </td>
   <td style="text-align:center;"> 7.39 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2004 </td>
   <td style="text-align:center;"> 6.43 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 6.56 </td>
   <td style="text-align:center;"> 0.89 </td>
   <td style="text-align:center;"> 7.44 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2005 </td>
   <td style="text-align:center;"> 6.33 </td>
   <td style="text-align:center;"> 0.84 </td>
   <td style="text-align:center;"> 6.12 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 7.65 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2006 </td>
   <td style="text-align:center;"> 6.08 </td>
   <td style="text-align:center;"> 0.79 </td>
   <td style="text-align:center;"> 5.69 </td>
   <td style="text-align:center;"> 0.74 </td>
   <td style="text-align:center;"> 7.78 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2007 </td>
   <td style="text-align:center;"> 5.64 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 6.02 </td>
   <td style="text-align:center;"> 0.77 </td>
   <td style="text-align:center;"> 7.88 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2008 </td>
   <td style="text-align:center;"> 5.61 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 5.98 </td>
   <td style="text-align:center;"> 0.78 </td>
   <td style="text-align:center;"> 7.76 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2009 </td>
   <td style="text-align:center;"> 7.07 </td>
   <td style="text-align:center;"> 0.93 </td>
   <td style="text-align:center;"> 6.87 </td>
   <td style="text-align:center;"> 0.90 </td>
   <td style="text-align:center;"> 7.75 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2010 </td>
   <td style="text-align:center;"> 7.03 </td>
   <td style="text-align:center;"> 0.90 </td>
   <td style="text-align:center;"> 6.41 </td>
   <td style="text-align:center;"> 0.82 </td>
   <td style="text-align:center;"> 7.80 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2011 </td>
   <td style="text-align:center;"> 5.57 </td>
   <td style="text-align:center;"> 0.71 </td>
   <td style="text-align:center;"> 4.95 </td>
   <td style="text-align:center;"> 0.63 </td>
   <td style="text-align:center;"> 7.95 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2012 </td>
   <td style="text-align:center;"> 5.57 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 5.05 </td>
   <td style="text-align:center;"> 0.63 </td>
   <td style="text-align:center;"> 8.04 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2013 </td>
   <td style="text-align:center;"> 4.88 </td>
   <td style="text-align:center;"> 0.60 </td>
   <td style="text-align:center;"> 5.33 </td>
   <td style="text-align:center;"> 0.65 </td>
   <td style="text-align:center;"> 8.23 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2014 </td>
   <td style="text-align:center;"> 5.50 </td>
   <td style="text-align:center;"> 0.67 </td>
   <td style="text-align:center;"> 5.67 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 8.17 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2015 </td>
   <td style="text-align:center;"> 5.27 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 6.04 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 8.26 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2016 </td>
   <td style="text-align:center;"> 5.90 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 6.10 </td>
   <td style="text-align:center;"> 0.76 </td>
   <td style="text-align:center;"> 8.18 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2017 </td>
   <td style="text-align:center;"> 5.40 </td>
   <td style="text-align:center;"> 0.65 </td>
   <td style="text-align:center;"> 5.63 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 8.44 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2018 </td>
   <td style="text-align:center;"> 5.92 </td>
   <td style="text-align:center;"> 0.72 </td>
   <td style="text-align:center;"> 5.71 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 8.46 </td>
  </tr>
</tbody>
</table>

The distribution of runs scored in a game is as follows. Most game teams score between 1 and 6 runs in a given game. Home teams are more likely to score 2+ runs, but do not have quite as many outlier, high run, games.  

![](Run-Environment_files/figure-html/runs by game distribution-1.png)<!-- -->

Looking at run scoring by inning we can see the most runs are scored in the 6th inning, followed by the bottom of the 3rd, 1st, and 8th innings. The 2nd and 9th innings are the lowest run scoring innings. This is likely due to the lower part of an order taking at bats in the 2nd inning and facing a closer in the 9th. 
<table class="table table-striped table-hover" style="font-size: 12px; margin-left: auto; margin-right: auto;">
<caption style="font-size: initial !important;">Runs Per Inning</caption>
 <thead>
  <tr>
   <th style="text-align:center;"> Year </th>
   <th style="text-align:center;"> top_1_mean </th>
   <th style="text-align:center;"> top_2_mean </th>
   <th style="text-align:center;"> top_3_mean </th>
   <th style="text-align:center;"> top_4_mean </th>
   <th style="text-align:center;"> top_5_mean </th>
   <th style="text-align:center;"> top_6_mean </th>
   <th style="text-align:center;"> top_7_mean </th>
   <th style="text-align:center;"> top_8_mean </th>
   <th style="text-align:center;"> top_9_mean </th>
   <th style="text-align:center;"> bot_1_mean </th>
   <th style="text-align:center;"> bot_2_mean </th>
   <th style="text-align:center;"> bot_3_mean </th>
   <th style="text-align:center;"> bot_4_mean </th>
   <th style="text-align:center;"> bot_5_mean </th>
   <th style="text-align:center;"> bot_6_mean </th>
   <th style="text-align:center;"> bot_7_mean </th>
   <th style="text-align:center;"> bot_8_mean </th>
   <th style="text-align:center;"> bot_9_mean </th>
   <th style="text-align:center;"> top_1_sd </th>
   <th style="text-align:center;"> top_2_sd </th>
   <th style="text-align:center;"> top_3_sd </th>
   <th style="text-align:center;"> top_4_sd </th>
   <th style="text-align:center;"> top_5_sd </th>
   <th style="text-align:center;"> top_6_sd </th>
   <th style="text-align:center;"> top_7_sd </th>
   <th style="text-align:center;"> top_8_sd </th>
   <th style="text-align:center;"> top_9_sd </th>
   <th style="text-align:center;"> bot_1_sd </th>
   <th style="text-align:center;"> bot_2_sd </th>
   <th style="text-align:center;"> bot_3_sd </th>
   <th style="text-align:center;"> bot_4_sd </th>
   <th style="text-align:center;"> bot_5_sd </th>
   <th style="text-align:center;"> bot_6_sd </th>
   <th style="text-align:center;"> bot_7_sd </th>
   <th style="text-align:center;"> bot_8_sd </th>
   <th style="text-align:center;"> bot_9_sd </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 2002 </td>
   <td style="text-align:center;"> 0.79 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.98 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.95 </td>
   <td style="text-align:center;"> 0.96 </td>
   <td style="text-align:center;"> 0.85 </td>
   <td style="text-align:center;"> 0.78 </td>
   <td style="text-align:center;"> 0.58 </td>
   <td style="text-align:center;"> 0.90 </td>
   <td style="text-align:center;"> 0.76 </td>
   <td style="text-align:center;"> 1.18 </td>
   <td style="text-align:center;"> 0.98 </td>
   <td style="text-align:center;"> 0.82 </td>
   <td style="text-align:center;"> 1.04 </td>
   <td style="text-align:center;"> 0.72 </td>
   <td style="text-align:center;"> 0.79 </td>
   <td style="text-align:center;"> 0.52 </td>
   <td style="text-align:center;"> 1.36 </td>
   <td style="text-align:center;"> 1.48 </td>
   <td style="text-align:center;"> 1.65 </td>
   <td style="text-align:center;"> 1.48 </td>
   <td style="text-align:center;"> 1.47 </td>
   <td style="text-align:center;"> 1.62 </td>
   <td style="text-align:center;"> 1.59 </td>
   <td style="text-align:center;"> 1.41 </td>
   <td style="text-align:center;"> 0.90 </td>
   <td style="text-align:center;"> 1.44 </td>
   <td style="text-align:center;"> 1.27 </td>
   <td style="text-align:center;"> 1.96 </td>
   <td style="text-align:center;"> 1.73 </td>
   <td style="text-align:center;"> 1.39 </td>
   <td style="text-align:center;"> 1.79 </td>
   <td style="text-align:center;"> 1.29 </td>
   <td style="text-align:center;"> 1.19 </td>
   <td style="text-align:center;"> 0.95 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2003 </td>
   <td style="text-align:center;"> 0.84 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 0.93 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.79 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.85 </td>
   <td style="text-align:center;"> 0.97 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 0.91 </td>
   <td style="text-align:center;"> 0.84 </td>
   <td style="text-align:center;"> 0.96 </td>
   <td style="text-align:center;"> 0.79 </td>
   <td style="text-align:center;"> 1.05 </td>
   <td style="text-align:center;"> 0.94 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 0.60 </td>
   <td style="text-align:center;"> 0.78 </td>
   <td style="text-align:center;"> 1.28 </td>
   <td style="text-align:center;"> 1.14 </td>
   <td style="text-align:center;"> 1.58 </td>
   <td style="text-align:center;"> 1.42 </td>
   <td style="text-align:center;"> 1.41 </td>
   <td style="text-align:center;"> 1.26 </td>
   <td style="text-align:center;"> 1.46 </td>
   <td style="text-align:center;"> 1.61 </td>
   <td style="text-align:center;"> 1.79 </td>
   <td style="text-align:center;"> 1.53 </td>
   <td style="text-align:center;"> 1.39 </td>
   <td style="text-align:center;"> 1.69 </td>
   <td style="text-align:center;"> 1.35 </td>
   <td style="text-align:center;"> 1.73 </td>
   <td style="text-align:center;"> 1.73 </td>
   <td style="text-align:center;"> 1.14 </td>
   <td style="text-align:center;"> 1.01 </td>
   <td style="text-align:center;"> 1.02 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2004 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 0.78 </td>
   <td style="text-align:center;"> 0.88 </td>
   <td style="text-align:center;"> 0.86 </td>
   <td style="text-align:center;"> 1.09 </td>
   <td style="text-align:center;"> 0.90 </td>
   <td style="text-align:center;"> 0.74 </td>
   <td style="text-align:center;"> 0.99 </td>
   <td style="text-align:center;"> 0.91 </td>
   <td style="text-align:center;"> 0.95 </td>
   <td style="text-align:center;"> 0.83 </td>
   <td style="text-align:center;"> 0.93 </td>
   <td style="text-align:center;"> 0.95 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 0.94 </td>
   <td style="text-align:center;"> 0.83 </td>
   <td style="text-align:center;"> 0.79 </td>
   <td style="text-align:center;"> 0.97 </td>
   <td style="text-align:center;"> 1.44 </td>
   <td style="text-align:center;"> 1.53 </td>
   <td style="text-align:center;"> 1.62 </td>
   <td style="text-align:center;"> 1.39 </td>
   <td style="text-align:center;"> 1.80 </td>
   <td style="text-align:center;"> 1.43 </td>
   <td style="text-align:center;"> 1.39 </td>
   <td style="text-align:center;"> 1.60 </td>
   <td style="text-align:center;"> 1.53 </td>
   <td style="text-align:center;"> 1.45 </td>
   <td style="text-align:center;"> 1.41 </td>
   <td style="text-align:center;"> 1.63 </td>
   <td style="text-align:center;"> 1.54 </td>
   <td style="text-align:center;"> 1.60 </td>
   <td style="text-align:center;"> 1.38 </td>
   <td style="text-align:center;"> 1.39 </td>
   <td style="text-align:center;"> 1.40 </td>
   <td style="text-align:center;"> 1.08 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2005 </td>
   <td style="text-align:center;"> 0.93 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 0.96 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 0.93 </td>
   <td style="text-align:center;"> 0.72 </td>
   <td style="text-align:center;"> 0.74 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 0.74 </td>
   <td style="text-align:center;"> 0.94 </td>
   <td style="text-align:center;"> 1.01 </td>
   <td style="text-align:center;"> 1.03 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 0.85 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 1.41 </td>
   <td style="text-align:center;"> 1.24 </td>
   <td style="text-align:center;"> 1.38 </td>
   <td style="text-align:center;"> 1.47 </td>
   <td style="text-align:center;"> 1.36 </td>
   <td style="text-align:center;"> 1.67 </td>
   <td style="text-align:center;"> 1.30 </td>
   <td style="text-align:center;"> 1.25 </td>
   <td style="text-align:center;"> 1.24 </td>
   <td style="text-align:center;"> 1.35 </td>
   <td style="text-align:center;"> 1.33 </td>
   <td style="text-align:center;"> 1.39 </td>
   <td style="text-align:center;"> 1.77 </td>
   <td style="text-align:center;"> 1.57 </td>
   <td style="text-align:center;"> 1.46 </td>
   <td style="text-align:center;"> 1.24 </td>
   <td style="text-align:center;"> 1.43 </td>
   <td style="text-align:center;"> 1.09 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2006 </td>
   <td style="text-align:center;"> 0.88 </td>
   <td style="text-align:center;"> 0.63 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 0.82 </td>
   <td style="text-align:center;"> 0.59 </td>
   <td style="text-align:center;"> 0.84 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 0.54 </td>
   <td style="text-align:center;"> 0.99 </td>
   <td style="text-align:center;"> 0.94 </td>
   <td style="text-align:center;"> 0.86 </td>
   <td style="text-align:center;"> 0.79 </td>
   <td style="text-align:center;"> 0.85 </td>
   <td style="text-align:center;"> 0.82 </td>
   <td style="text-align:center;"> 0.91 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 0.62 </td>
   <td style="text-align:center;"> 1.38 </td>
   <td style="text-align:center;"> 1.12 </td>
   <td style="text-align:center;"> 1.29 </td>
   <td style="text-align:center;"> 1.46 </td>
   <td style="text-align:center;"> 1.06 </td>
   <td style="text-align:center;"> 1.45 </td>
   <td style="text-align:center;"> 1.21 </td>
   <td style="text-align:center;"> 1.03 </td>
   <td style="text-align:center;"> 1.53 </td>
   <td style="text-align:center;"> 1.62 </td>
   <td style="text-align:center;"> 1.64 </td>
   <td style="text-align:center;"> 1.38 </td>
   <td style="text-align:center;"> 1.41 </td>
   <td style="text-align:center;"> 1.41 </td>
   <td style="text-align:center;"> 1.48 </td>
   <td style="text-align:center;"> 1.17 </td>
   <td style="text-align:center;"> 1.27 </td>
   <td style="text-align:center;"> 1.21 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2007 </td>
   <td style="text-align:center;"> 0.67 </td>
   <td style="text-align:center;"> 0.65 </td>
   <td style="text-align:center;"> 0.67 </td>
   <td style="text-align:center;"> 0.72 </td>
   <td style="text-align:center;"> 0.90 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.84 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 0.76 </td>
   <td style="text-align:center;"> 0.82 </td>
   <td style="text-align:center;"> 0.71 </td>
   <td style="text-align:center;"> 0.82 </td>
   <td style="text-align:center;"> 0.71 </td>
   <td style="text-align:center;"> 0.85 </td>
   <td style="text-align:center;"> 0.82 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 0.47 </td>
   <td style="text-align:center;"> 1.14 </td>
   <td style="text-align:center;"> 1.21 </td>
   <td style="text-align:center;"> 1.26 </td>
   <td style="text-align:center;"> 1.34 </td>
   <td style="text-align:center;"> 1.61 </td>
   <td style="text-align:center;"> 1.48 </td>
   <td style="text-align:center;"> 1.56 </td>
   <td style="text-align:center;"> 1.51 </td>
   <td style="text-align:center;"> 1.45 </td>
   <td style="text-align:center;"> 1.41 </td>
   <td style="text-align:center;"> 1.13 </td>
   <td style="text-align:center;"> 1.40 </td>
   <td style="text-align:center;"> 1.31 </td>
   <td style="text-align:center;"> 1.53 </td>
   <td style="text-align:center;"> 1.53 </td>
   <td style="text-align:center;"> 1.50 </td>
   <td style="text-align:center;"> 1.20 </td>
   <td style="text-align:center;"> 1.18 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2008 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 0.79 </td>
   <td style="text-align:center;"> 0.71 </td>
   <td style="text-align:center;"> 0.84 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 0.84 </td>
   <td style="text-align:center;"> 0.58 </td>
   <td style="text-align:center;"> 0.52 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.86 </td>
   <td style="text-align:center;"> 0.83 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.74 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 0.72 </td>
   <td style="text-align:center;"> 0.46 </td>
   <td style="text-align:center;"> 1.42 </td>
   <td style="text-align:center;"> 1.34 </td>
   <td style="text-align:center;"> 1.28 </td>
   <td style="text-align:center;"> 1.55 </td>
   <td style="text-align:center;"> 1.42 </td>
   <td style="text-align:center;"> 1.38 </td>
   <td style="text-align:center;"> 1.34 </td>
   <td style="text-align:center;"> 1.16 </td>
   <td style="text-align:center;"> 1.15 </td>
   <td style="text-align:center;"> 1.36 </td>
   <td style="text-align:center;"> 1.41 </td>
   <td style="text-align:center;"> 1.44 </td>
   <td style="text-align:center;"> 1.50 </td>
   <td style="text-align:center;"> 1.47 </td>
   <td style="text-align:center;"> 1.38 </td>
   <td style="text-align:center;"> 1.28 </td>
   <td style="text-align:center;"> 1.25 </td>
   <td style="text-align:center;"> 0.84 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2009 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 0.90 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 0.99 </td>
   <td style="text-align:center;"> 0.91 </td>
   <td style="text-align:center;"> 0.96 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 0.97 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 0.97 </td>
   <td style="text-align:center;"> 0.91 </td>
   <td style="text-align:center;"> 1.11 </td>
   <td style="text-align:center;"> 1.06 </td>
   <td style="text-align:center;"> 0.86 </td>
   <td style="text-align:center;"> 0.82 </td>
   <td style="text-align:center;"> 0.49 </td>
   <td style="text-align:center;"> 1.42 </td>
   <td style="text-align:center;"> 1.72 </td>
   <td style="text-align:center;"> 1.27 </td>
   <td style="text-align:center;"> 1.28 </td>
   <td style="text-align:center;"> 1.66 </td>
   <td style="text-align:center;"> 1.75 </td>
   <td style="text-align:center;"> 1.48 </td>
   <td style="text-align:center;"> 1.54 </td>
   <td style="text-align:center;"> 1.24 </td>
   <td style="text-align:center;"> 1.58 </td>
   <td style="text-align:center;"> 1.71 </td>
   <td style="text-align:center;"> 1.62 </td>
   <td style="text-align:center;"> 1.68 </td>
   <td style="text-align:center;"> 1.75 </td>
   <td style="text-align:center;"> 1.70 </td>
   <td style="text-align:center;"> 1.49 </td>
   <td style="text-align:center;"> 1.29 </td>
   <td style="text-align:center;"> 0.97 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2010 </td>
   <td style="text-align:center;"> 1.08 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 0.79 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 0.90 </td>
   <td style="text-align:center;"> 0.95 </td>
   <td style="text-align:center;"> 0.80 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 0.61 </td>
   <td style="text-align:center;"> 1.03 </td>
   <td style="text-align:center;"> 1.03 </td>
   <td style="text-align:center;"> 0.94 </td>
   <td style="text-align:center;"> 1.05 </td>
   <td style="text-align:center;"> 1.08 </td>
   <td style="text-align:center;"> 0.85 </td>
   <td style="text-align:center;"> 0.80 </td>
   <td style="text-align:center;"> 0.89 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 1.65 </td>
   <td style="text-align:center;"> 1.27 </td>
   <td style="text-align:center;"> 1.33 </td>
   <td style="text-align:center;"> 1.41 </td>
   <td style="text-align:center;"> 1.58 </td>
   <td style="text-align:center;"> 1.64 </td>
   <td style="text-align:center;"> 1.31 </td>
   <td style="text-align:center;"> 1.28 </td>
   <td style="text-align:center;"> 1.04 </td>
   <td style="text-align:center;"> 1.66 </td>
   <td style="text-align:center;"> 1.79 </td>
   <td style="text-align:center;"> 1.53 </td>
   <td style="text-align:center;"> 1.62 </td>
   <td style="text-align:center;"> 1.58 </td>
   <td style="text-align:center;"> 1.49 </td>
   <td style="text-align:center;"> 1.37 </td>
   <td style="text-align:center;"> 1.54 </td>
   <td style="text-align:center;"> 1.01 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2011 </td>
   <td style="text-align:center;"> 0.61 </td>
   <td style="text-align:center;"> 0.44 </td>
   <td style="text-align:center;"> 0.62 </td>
   <td style="text-align:center;"> 0.56 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.74 </td>
   <td style="text-align:center;"> 0.39 </td>
   <td style="text-align:center;"> 0.59 </td>
   <td style="text-align:center;"> 0.92 </td>
   <td style="text-align:center;"> 0.67 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.76 </td>
   <td style="text-align:center;"> 0.71 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 0.85 </td>
   <td style="text-align:center;"> 0.47 </td>
   <td style="text-align:center;"> 1.17 </td>
   <td style="text-align:center;"> 0.97 </td>
   <td style="text-align:center;"> 1.24 </td>
   <td style="text-align:center;"> 1.14 </td>
   <td style="text-align:center;"> 1.30 </td>
   <td style="text-align:center;"> 1.46 </td>
   <td style="text-align:center;"> 1.61 </td>
   <td style="text-align:center;"> 0.83 </td>
   <td style="text-align:center;"> 1.06 </td>
   <td style="text-align:center;"> 1.61 </td>
   <td style="text-align:center;"> 1.30 </td>
   <td style="text-align:center;"> 1.27 </td>
   <td style="text-align:center;"> 1.34 </td>
   <td style="text-align:center;"> 1.29 </td>
   <td style="text-align:center;"> 1.27 </td>
   <td style="text-align:center;"> 1.46 </td>
   <td style="text-align:center;"> 1.45 </td>
   <td style="text-align:center;"> 0.80 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2012 </td>
   <td style="text-align:center;"> 0.57 </td>
   <td style="text-align:center;"> 0.63 </td>
   <td style="text-align:center;"> 0.57 </td>
   <td style="text-align:center;"> 0.59 </td>
   <td style="text-align:center;"> 0.76 </td>
   <td style="text-align:center;"> 0.65 </td>
   <td style="text-align:center;"> 0.63 </td>
   <td style="text-align:center;"> 0.56 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 0.74 </td>
   <td style="text-align:center;"> 0.83 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.72 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.57 </td>
   <td style="text-align:center;"> 0.93 </td>
   <td style="text-align:center;"> 0.36 </td>
   <td style="text-align:center;"> 1.04 </td>
   <td style="text-align:center;"> 1.34 </td>
   <td style="text-align:center;"> 1.17 </td>
   <td style="text-align:center;"> 1.29 </td>
   <td style="text-align:center;"> 1.32 </td>
   <td style="text-align:center;"> 1.23 </td>
   <td style="text-align:center;"> 1.33 </td>
   <td style="text-align:center;"> 1.11 </td>
   <td style="text-align:center;"> 1.05 </td>
   <td style="text-align:center;"> 1.37 </td>
   <td style="text-align:center;"> 1.73 </td>
   <td style="text-align:center;"> 1.22 </td>
   <td style="text-align:center;"> 1.29 </td>
   <td style="text-align:center;"> 1.52 </td>
   <td style="text-align:center;"> 1.30 </td>
   <td style="text-align:center;"> 1.05 </td>
   <td style="text-align:center;"> 1.45 </td>
   <td style="text-align:center;"> 0.67 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2013 </td>
   <td style="text-align:center;"> 0.71 </td>
   <td style="text-align:center;"> 0.53 </td>
   <td style="text-align:center;"> 0.72 </td>
   <td style="text-align:center;"> 0.72 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 0.59 </td>
   <td style="text-align:center;"> 0.52 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 0.76 </td>
   <td style="text-align:center;"> 0.48 </td>
   <td style="text-align:center;"> 0.62 </td>
   <td style="text-align:center;"> 0.58 </td>
   <td style="text-align:center;"> 0.76 </td>
   <td style="text-align:center;"> 0.71 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.56 </td>
   <td style="text-align:center;"> 0.25 </td>
   <td style="text-align:center;"> 1.26 </td>
   <td style="text-align:center;"> 1.21 </td>
   <td style="text-align:center;"> 1.30 </td>
   <td style="text-align:center;"> 1.37 </td>
   <td style="text-align:center;"> 1.23 </td>
   <td style="text-align:center;"> 1.17 </td>
   <td style="text-align:center;"> 1.04 </td>
   <td style="text-align:center;"> 1.11 </td>
   <td style="text-align:center;"> 1.18 </td>
   <td style="text-align:center;"> 1.37 </td>
   <td style="text-align:center;"> 1.03 </td>
   <td style="text-align:center;"> 1.18 </td>
   <td style="text-align:center;"> 1.04 </td>
   <td style="text-align:center;"> 1.36 </td>
   <td style="text-align:center;"> 1.31 </td>
   <td style="text-align:center;"> 1.10 </td>
   <td style="text-align:center;"> 1.04 </td>
   <td style="text-align:center;"> 0.61 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2014 </td>
   <td style="text-align:center;"> 0.77 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 0.65 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.80 </td>
   <td style="text-align:center;"> 0.61 </td>
   <td style="text-align:center;"> 0.61 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 0.80 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.67 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.53 </td>
   <td style="text-align:center;"> 0.79 </td>
   <td style="text-align:center;"> 0.52 </td>
   <td style="text-align:center;"> 1.41 </td>
   <td style="text-align:center;"> 1.51 </td>
   <td style="text-align:center;"> 1.11 </td>
   <td style="text-align:center;"> 1.37 </td>
   <td style="text-align:center;"> 1.10 </td>
   <td style="text-align:center;"> 1.33 </td>
   <td style="text-align:center;"> 1.15 </td>
   <td style="text-align:center;"> 1.21 </td>
   <td style="text-align:center;"> 1.14 </td>
   <td style="text-align:center;"> 1.35 </td>
   <td style="text-align:center;"> 1.44 </td>
   <td style="text-align:center;"> 1.54 </td>
   <td style="text-align:center;"> 1.15 </td>
   <td style="text-align:center;"> 1.21 </td>
   <td style="text-align:center;"> 1.47 </td>
   <td style="text-align:center;"> 1.14 </td>
   <td style="text-align:center;"> 1.21 </td>
   <td style="text-align:center;"> 1.05 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2015 </td>
   <td style="text-align:center;"> 0.62 </td>
   <td style="text-align:center;"> 0.58 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.77 </td>
   <td style="text-align:center;"> 0.90 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.85 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 0.77 </td>
   <td style="text-align:center;"> 0.46 </td>
   <td style="text-align:center;"> 0.72 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 0.59 </td>
   <td style="text-align:center;"> 1.21 </td>
   <td style="text-align:center;"> 1.31 </td>
   <td style="text-align:center;"> 1.31 </td>
   <td style="text-align:center;"> 1.38 </td>
   <td style="text-align:center;"> 1.38 </td>
   <td style="text-align:center;"> 1.52 </td>
   <td style="text-align:center;"> 1.29 </td>
   <td style="text-align:center;"> 1.58 </td>
   <td style="text-align:center;"> 1.32 </td>
   <td style="text-align:center;"> 1.36 </td>
   <td style="text-align:center;"> 0.94 </td>
   <td style="text-align:center;"> 1.34 </td>
   <td style="text-align:center;"> 1.20 </td>
   <td style="text-align:center;"> 1.25 </td>
   <td style="text-align:center;"> 1.35 </td>
   <td style="text-align:center;"> 1.08 </td>
   <td style="text-align:center;"> 1.24 </td>
   <td style="text-align:center;"> 0.82 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2016 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 0.63 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.93 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 0.67 </td>
   <td style="text-align:center;"> 0.77 </td>
   <td style="text-align:center;"> 0.90 </td>
   <td style="text-align:center;"> 0.78 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 0.77 </td>
   <td style="text-align:center;"> 0.72 </td>
   <td style="text-align:center;"> 1.37 </td>
   <td style="text-align:center;"> 1.30 </td>
   <td style="text-align:center;"> 1.06 </td>
   <td style="text-align:center;"> 1.34 </td>
   <td style="text-align:center;"> 1.34 </td>
   <td style="text-align:center;"> 1.54 </td>
   <td style="text-align:center;"> 1.39 </td>
   <td style="text-align:center;"> 1.14 </td>
   <td style="text-align:center;"> 1.21 </td>
   <td style="text-align:center;"> 1.18 </td>
   <td style="text-align:center;"> 1.52 </td>
   <td style="text-align:center;"> 1.64 </td>
   <td style="text-align:center;"> 1.45 </td>
   <td style="text-align:center;"> 1.16 </td>
   <td style="text-align:center;"> 1.43 </td>
   <td style="text-align:center;"> 1.49 </td>
   <td style="text-align:center;"> 1.33 </td>
   <td style="text-align:center;"> 1.24 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2017 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 0.49 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 0.79 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 0.67 </td>
   <td style="text-align:center;"> 0.85 </td>
   <td style="text-align:center;"> 0.58 </td>
   <td style="text-align:center;"> 0.80 </td>
   <td style="text-align:center;"> 0.59 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.62 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 0.72 </td>
   <td style="text-align:center;"> 0.52 </td>
   <td style="text-align:center;"> 1.31 </td>
   <td style="text-align:center;"> 1.02 </td>
   <td style="text-align:center;"> 1.32 </td>
   <td style="text-align:center;"> 1.37 </td>
   <td style="text-align:center;"> 1.25 </td>
   <td style="text-align:center;"> 1.31 </td>
   <td style="text-align:center;"> 1.22 </td>
   <td style="text-align:center;"> 1.50 </td>
   <td style="text-align:center;"> 1.09 </td>
   <td style="text-align:center;"> 1.53 </td>
   <td style="text-align:center;"> 1.22 </td>
   <td style="text-align:center;"> 1.17 </td>
   <td style="text-align:center;"> 1.30 </td>
   <td style="text-align:center;"> 1.26 </td>
   <td style="text-align:center;"> 1.42 </td>
   <td style="text-align:center;"> 1.25 </td>
   <td style="text-align:center;"> 1.26 </td>
   <td style="text-align:center;"> 0.88 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2018 </td>
   <td style="text-align:center;"> 0.63 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 0.77 </td>
   <td style="text-align:center;"> 0.52 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 0.67 </td>
   <td style="text-align:center;"> 0.76 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.56 </td>
   <td style="text-align:center;"> 0.76 </td>
   <td style="text-align:center;"> 0.80 </td>
   <td style="text-align:center;"> 0.65 </td>
   <td style="text-align:center;"> 0.96 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.65 </td>
   <td style="text-align:center;"> 1.17 </td>
   <td style="text-align:center;"> 1.18 </td>
   <td style="text-align:center;"> 1.26 </td>
   <td style="text-align:center;"> 1.03 </td>
   <td style="text-align:center;"> 1.12 </td>
   <td style="text-align:center;"> 1.34 </td>
   <td style="text-align:center;"> 1.43 </td>
   <td style="text-align:center;"> 1.34 </td>
   <td style="text-align:center;"> 1.42 </td>
   <td style="text-align:center;"> 1.41 </td>
   <td style="text-align:center;"> 1.21 </td>
   <td style="text-align:center;"> 1.43 </td>
   <td style="text-align:center;"> 1.58 </td>
   <td style="text-align:center;"> 1.32 </td>
   <td style="text-align:center;"> 1.81 </td>
   <td style="text-align:center;"> 1.23 </td>
   <td style="text-align:center;"> 1.59 </td>
   <td style="text-align:center;"> 1.22 </td>
  </tr>
</tbody>
</table>

![](Run-Environment_files/figure-html/runs by inning summary-1.png)<!-- -->


## Advanced

While looking at run scoring for games and innings is important, it lacks much of the context for what happened in each inning. To better understand how runs are scored in any given inning, and how many runs to expect in any situation, we must take a closer look at the context for which runs are scored. The context of a baseball game consists of innings, outs, and bases. Within every inning there are three outs and three bases which can be occupied during those outs. Therefore, there are 24 base/out states in an given inning. For instance, one possible state is a runner on second and third with one out. These base/out states give context for how runs are scored within an inning. 

### Run Expectancy

Using play-by-play data from the 2017-2019 we can find the run expectancy for any of the 24 base/out states. On average, when a team starts an inning (base/out state of nobody on, nobody out) a team will score 0.66 runs before the inning ends. If the leadoff hitter hits a double the run expectancy jumps to 1.49 runs until the end of the inning. As the base/out state transitioned, so did the run expectancy which increased by 0.83 runs. The double was the event that triggered the state change and is worth 0.83 runs on average. It doesn't matter if the event was a double or a single with an error that led to a runner on second with no outs, the event is worth 0.83 runs. The following is run expectancy for all 24 base/out states in the ARC.

<table class="table table-striped table-hover" style="font-size: 12px; margin-left: auto; margin-right: auto;">
<caption style="font-size: initial !important;">Run Expectancy</caption>
 <thead>
  <tr>
   <th style="text-align:center;"> Base </th>
   <th style="text-align:center;"> 0 Outs </th>
   <th style="text-align:center;"> 1 Out </th>
   <th style="text-align:center;"> 2 Outs </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 000 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.33 </td>
   <td style="text-align:center;"> 0.11 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 100 </td>
   <td style="text-align:center;"> 1.15 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.26 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 010 </td>
   <td style="text-align:center;"> 1.49 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 0.39 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 001 </td>
   <td style="text-align:center;"> 1.68 </td>
   <td style="text-align:center;"> 1.19 </td>
   <td style="text-align:center;"> 0.45 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 110 </td>
   <td style="text-align:center;"> 1.93 </td>
   <td style="text-align:center;"> 1.21 </td>
   <td style="text-align:center;"> 0.51 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 101 </td>
   <td style="text-align:center;"> 2.13 </td>
   <td style="text-align:center;"> 1.44 </td>
   <td style="text-align:center;"> 0.64 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 011 </td>
   <td style="text-align:center;"> 2.43 </td>
   <td style="text-align:center;"> 1.56 </td>
   <td style="text-align:center;"> 0.78 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 111 </td>
   <td style="text-align:center;"> 2.70 </td>
   <td style="text-align:center;"> 1.90 </td>
   <td style="text-align:center;"> 0.96 </td>
  </tr>
</tbody>
</table>

Using the run expectancy matrix we can evaluate how a successful bunt changes run expectancy. Consider the sacrifice bunting situation of a runner on first with no outs, on average teams will score 1.15 runs in the inning. A successful sacrifice bunt leaves the state at runner on second with one out and a run expectancy of 0.87. So the sacrifice bunt *lowers* run expectancy by 0.28 runs in the inning! Another application is evaluating steal attempts. What if the team attempts a stolen base instead of the sacrifice bunt? If the stolen base is successful, the new state is runner on second nobody out which has a run expectancy of 1.49 (an increase of 0.34 runs). If the attempt is unsuccessful, the new state is bases empty one out with a run expectancy of 0.33 (a decrease of 0.82 runs). To even have a positive expected run value for a stolen base in this situation, a team has to be successful 71% of the time ($EV = 0.34p - 0.84(1-p)$ where $p$ is the probability of success). We must note that this run expectancy is based on average situations - average hitters, average pitching, and average fielders.

### Run Values

Using the run expectancy matrix we can find the average run value of any event (single, double, stolen base, etc.). The run values for these events can then be used to calculate a context-neutral run value of any player based on more standard accumulated stats. When evaluating the run value of an event it's important to account for the context of the event. For instance, a sacrifice bunt is typically performed with runners on base and no out which have higher run expectancies than the start of an inning. To find the run value of an event we calculate the average number of runs scored until the end of the inning after the event and substract the starting run expectancy.

<table class="table table-striped table-hover" style="font-size: 12px; margin-left: auto; margin-right: auto;">
<caption style="font-size: initial !important;">Run Value</caption>
 <thead>
  <tr>
   <th style="text-align:center;"> Event </th>
   <th style="text-align:center;"> N </th>
   <th style="text-align:center;"> Runs to End 
of Inning </th>
   <th style="text-align:center;"> Average 
Runs </th>
   <th style="text-align:center;"> Starting 
RE </th>
   <th style="text-align:center;"> Run 
Value </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> home run </td>
   <td style="text-align:center;"> 442 </td>
   <td style="text-align:center;"> 1008 </td>
   <td style="text-align:center;"> 2.28 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 1.59 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> triple </td>
   <td style="text-align:center;"> 379 </td>
   <td style="text-align:center;"> 738 </td>
   <td style="text-align:center;"> 1.95 </td>
   <td style="text-align:center;"> 0.72 </td>
   <td style="text-align:center;"> 1.23 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> double </td>
   <td style="text-align:center;"> 2417 </td>
   <td style="text-align:center;"> 3825 </td>
   <td style="text-align:center;"> 1.58 </td>
   <td style="text-align:center;"> 0.71 </td>
   <td style="text-align:center;"> 0.87 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> single </td>
   <td style="text-align:center;"> 9443 </td>
   <td style="text-align:center;"> 12003 </td>
   <td style="text-align:center;"> 1.27 </td>
   <td style="text-align:center;"> 0.72 </td>
   <td style="text-align:center;"> 0.55 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> error </td>
   <td style="text-align:center;"> 1647 </td>
   <td style="text-align:center;"> 2002 </td>
   <td style="text-align:center;"> 1.22 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 0.49 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> hit by pitch </td>
   <td style="text-align:center;"> 1516 </td>
   <td style="text-align:center;"> 1768 </td>
   <td style="text-align:center;"> 1.17 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 0.47 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> walk </td>
   <td style="text-align:center;"> 4778 </td>
   <td style="text-align:center;"> 5268 </td>
   <td style="text-align:center;"> 1.10 </td>
   <td style="text-align:center;"> 0.71 </td>
   <td style="text-align:center;"> 0.39 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> wild pitch </td>
   <td style="text-align:center;"> 1260 </td>
   <td style="text-align:center;"> 1627 </td>
   <td style="text-align:center;"> 1.29 </td>
   <td style="text-align:center;"> 0.90 </td>
   <td style="text-align:center;"> 0.39 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> balk </td>
   <td style="text-align:center;"> 171 </td>
   <td style="text-align:center;"> 208 </td>
   <td style="text-align:center;"> 1.22 </td>
   <td style="text-align:center;"> 0.94 </td>
   <td style="text-align:center;"> 0.28 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> pickoff error </td>
   <td style="text-align:center;"> 88 </td>
   <td style="text-align:center;"> 106 </td>
   <td style="text-align:center;"> 1.20 </td>
   <td style="text-align:center;"> 0.92 </td>
   <td style="text-align:center;"> 0.28 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> interference </td>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 0.83 </td>
   <td style="text-align:center;"> 0.57 </td>
   <td style="text-align:center;"> 0.26 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> passed ball </td>
   <td style="text-align:center;"> 401 </td>
   <td style="text-align:center;"> 432 </td>
   <td style="text-align:center;"> 1.08 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 0.21 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> stolen base </td>
   <td style="text-align:center;"> 1607 </td>
   <td style="text-align:center;"> 1577 </td>
   <td style="text-align:center;"> 0.98 </td>
   <td style="text-align:center;"> 0.78 </td>
   <td style="text-align:center;"> 0.20 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> generic out </td>
   <td style="text-align:center;"> 21292 </td>
   <td style="text-align:center;"> 6759 </td>
   <td style="text-align:center;"> 0.32 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> -0.36 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> fielder's choice </td>
   <td style="text-align:center;"> 1532 </td>
   <td style="text-align:center;"> 1029 </td>
   <td style="text-align:center;"> 0.67 </td>
   <td style="text-align:center;"> 1.06 </td>
   <td style="text-align:center;"> -0.39 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> strikeout </td>
   <td style="text-align:center;"> 8568 </td>
   <td style="text-align:center;"> 2318 </td>
   <td style="text-align:center;"> 0.27 </td>
   <td style="text-align:center;"> 0.67 </td>
   <td style="text-align:center;"> -0.40 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> caught stealing </td>
   <td style="text-align:center;"> 481 </td>
   <td style="text-align:center;"> 97 </td>
   <td style="text-align:center;"> 0.20 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> -0.55 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> pickoff </td>
   <td style="text-align:center;"> 290 </td>
   <td style="text-align:center;"> 81 </td>
   <td style="text-align:center;"> 0.28 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> -0.59 </td>
  </tr>
</tbody>
</table>

### Scoring Distributions

The run expectancy matrix gives the average runs expected until the end of an inning given any base/out state. However, we would also like to know the probability of scoring runs given any base out state. Back to the sacrifice bunt example, we know the sacrifice bunt lowers the run expectancy, but does it increase the probability of scoring one run? Below is the scoring distribution for all ARC team games from 2017-2019

<table class="table table-striped table-hover" style="font-size: 12px; margin-left: auto; margin-right: auto;">
<caption style="font-size: initial !important;">Scoring Distribution (%)</caption>
 <thead>
  <tr>
   <th style="text-align:center;"> State </th>
   <th style="text-align:center;"> RE </th>
   <th style="text-align:center;"> 0 Runs </th>
   <th style="text-align:center;"> 1 Run </th>
   <th style="text-align:center;"> 2 Runs </th>
   <th style="text-align:center;"> 3 Runs </th>
   <th style="text-align:center;"> 4+ Runs </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 000 0 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 67.6 </td>
   <td style="text-align:center;"> 16.0 </td>
   <td style="text-align:center;"> 8.0 </td>
   <td style="text-align:center;"> 4.3 </td>
   <td style="text-align:center;"> 4.1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 000 1 </td>
   <td style="text-align:center;"> 0.33 </td>
   <td style="text-align:center;"> 82.0 </td>
   <td style="text-align:center;"> 10.0 </td>
   <td style="text-align:center;"> 4.3 </td>
   <td style="text-align:center;"> 2.1 </td>
   <td style="text-align:center;"> 1.5 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 000 2 </td>
   <td style="text-align:center;"> 0.11 </td>
   <td style="text-align:center;"> 93.0 </td>
   <td style="text-align:center;"> 4.4 </td>
   <td style="text-align:center;"> 1.6 </td>
   <td style="text-align:center;"> 0.6 </td>
   <td style="text-align:center;"> 0.4 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 001 0 </td>
   <td style="text-align:center;"> 1.68 </td>
   <td style="text-align:center;"> 9.9 </td>
   <td style="text-align:center;"> 50.4 </td>
   <td style="text-align:center;"> 18.4 </td>
   <td style="text-align:center;"> 11.4 </td>
   <td style="text-align:center;"> 9.9 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 001 1 </td>
   <td style="text-align:center;"> 1.19 </td>
   <td style="text-align:center;"> 25.3 </td>
   <td style="text-align:center;"> 52.0 </td>
   <td style="text-align:center;"> 13.0 </td>
   <td style="text-align:center;"> 3.8 </td>
   <td style="text-align:center;"> 5.9 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 001 2 </td>
   <td style="text-align:center;"> 0.45 </td>
   <td style="text-align:center;"> 65.8 </td>
   <td style="text-align:center;"> 26.2 </td>
   <td style="text-align:center;"> 5.7 </td>
   <td style="text-align:center;"> 1.5 </td>
   <td style="text-align:center;"> 0.7 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 010 0 </td>
   <td style="text-align:center;"> 1.49 </td>
   <td style="text-align:center;"> 29.3 </td>
   <td style="text-align:center;"> 34.7 </td>
   <td style="text-align:center;"> 16.2 </td>
   <td style="text-align:center;"> 8.6 </td>
   <td style="text-align:center;"> 11.1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 010 1 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 51.3 </td>
   <td style="text-align:center;"> 27.9 </td>
   <td style="text-align:center;"> 11.3 </td>
   <td style="text-align:center;"> 5.2 </td>
   <td style="text-align:center;"> 4.3 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 010 2 </td>
   <td style="text-align:center;"> 0.39 </td>
   <td style="text-align:center;"> 73.8 </td>
   <td style="text-align:center;"> 17.9 </td>
   <td style="text-align:center;"> 5.5 </td>
   <td style="text-align:center;"> 1.8 </td>
   <td style="text-align:center;"> 1.0 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 011 0 </td>
   <td style="text-align:center;"> 2.43 </td>
   <td style="text-align:center;"> 10.3 </td>
   <td style="text-align:center;"> 20.4 </td>
   <td style="text-align:center;"> 32.8 </td>
   <td style="text-align:center;"> 15.5 </td>
   <td style="text-align:center;"> 21.0 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 011 1 </td>
   <td style="text-align:center;"> 1.56 </td>
   <td style="text-align:center;"> 26.4 </td>
   <td style="text-align:center;"> 28.3 </td>
   <td style="text-align:center;"> 26.1 </td>
   <td style="text-align:center;"> 10.0 </td>
   <td style="text-align:center;"> 9.2 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 011 2 </td>
   <td style="text-align:center;"> 0.78 </td>
   <td style="text-align:center;"> 64.7 </td>
   <td style="text-align:center;"> 9.7 </td>
   <td style="text-align:center;"> 16.5 </td>
   <td style="text-align:center;"> 4.9 </td>
   <td style="text-align:center;"> 4.2 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 100 0 </td>
   <td style="text-align:center;"> 1.15 </td>
   <td style="text-align:center;"> 48.6 </td>
   <td style="text-align:center;"> 21.7 </td>
   <td style="text-align:center;"> 13.9 </td>
   <td style="text-align:center;"> 7.6 </td>
   <td style="text-align:center;"> 8.2 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 100 1 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 67.1 </td>
   <td style="text-align:center;"> 15.3 </td>
   <td style="text-align:center;"> 9.2 </td>
   <td style="text-align:center;"> 4.7 </td>
   <td style="text-align:center;"> 3.7 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 100 2 </td>
   <td style="text-align:center;"> 0.26 </td>
   <td style="text-align:center;"> 84.7 </td>
   <td style="text-align:center;"> 8.7 </td>
   <td style="text-align:center;"> 3.9 </td>
   <td style="text-align:center;"> 1.8 </td>
   <td style="text-align:center;"> 0.9 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 101 0 </td>
   <td style="text-align:center;"> 2.13 </td>
   <td style="text-align:center;"> 9.6 </td>
   <td style="text-align:center;"> 36.3 </td>
   <td style="text-align:center;"> 22.5 </td>
   <td style="text-align:center;"> 13.6 </td>
   <td style="text-align:center;"> 18.0 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 101 1 </td>
   <td style="text-align:center;"> 1.44 </td>
   <td style="text-align:center;"> 26.6 </td>
   <td style="text-align:center;"> 37.5 </td>
   <td style="text-align:center;"> 17.6 </td>
   <td style="text-align:center;"> 9.4 </td>
   <td style="text-align:center;"> 8.8 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 101 2 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 63.2 </td>
   <td style="text-align:center;"> 21.5 </td>
   <td style="text-align:center;"> 9.1 </td>
   <td style="text-align:center;"> 3.7 </td>
   <td style="text-align:center;"> 2.5 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 110 0 </td>
   <td style="text-align:center;"> 1.93 </td>
   <td style="text-align:center;"> 27.0 </td>
   <td style="text-align:center;"> 23.7 </td>
   <td style="text-align:center;"> 20.0 </td>
   <td style="text-align:center;"> 11.8 </td>
   <td style="text-align:center;"> 17.5 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 110 1 </td>
   <td style="text-align:center;"> 1.21 </td>
   <td style="text-align:center;"> 48.6 </td>
   <td style="text-align:center;"> 17.6 </td>
   <td style="text-align:center;"> 15.4 </td>
   <td style="text-align:center;"> 9.6 </td>
   <td style="text-align:center;"> 8.9 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 110 2 </td>
   <td style="text-align:center;"> 0.51 </td>
   <td style="text-align:center;"> 74.1 </td>
   <td style="text-align:center;"> 11.4 </td>
   <td style="text-align:center;"> 7.4 </td>
   <td style="text-align:center;"> 4.5 </td>
   <td style="text-align:center;"> 2.6 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 111 0 </td>
   <td style="text-align:center;"> 2.70 </td>
   <td style="text-align:center;"> 12.0 </td>
   <td style="text-align:center;"> 20.9 </td>
   <td style="text-align:center;"> 19.4 </td>
   <td style="text-align:center;"> 15.2 </td>
   <td style="text-align:center;"> 32.5 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 111 1 </td>
   <td style="text-align:center;"> 1.90 </td>
   <td style="text-align:center;"> 26.2 </td>
   <td style="text-align:center;"> 25.4 </td>
   <td style="text-align:center;"> 18.1 </td>
   <td style="text-align:center;"> 13.0 </td>
   <td style="text-align:center;"> 17.3 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 111 2 </td>
   <td style="text-align:center;"> 0.96 </td>
   <td style="text-align:center;"> 59.2 </td>
   <td style="text-align:center;"> 13.3 </td>
   <td style="text-align:center;"> 12.6 </td>
   <td style="text-align:center;"> 7.4 </td>
   <td style="text-align:center;"> 7.5 </td>
  </tr>
</tbody>
</table>

With a runner on first and nobody out, an average team can expect to score zero runs 48.6% of the time and has a 21.7% chance of scoring exactly one run. A successful sacrifice bunt moving the runner to second with one out increases the probability of scoring zero runs to 51.3%, or a 2.7% increase and only increases the probability of scoring 1 run by 6.2% (from 21.7% to 27.9%), but decreases the probability of scoring 2 or more runs. A successful sacrifice bunt does slightly increase the chances of scoring one run, but it also increases the chance of scoring no runs because one of three outs was used. What if the sacrifice bunt is unsuccesful transitioning to a runner on first one out state? An unsuccessful bunt is very costly increasing the probability of scoring no runs from 48.6% to 67.1%, increasing the chance of not scoring by 18.5%! 

### Win Probability

We can expand our analysis to study how run differentials effect win probabilities. For any given inning, out, run differential state we find the probability that a team wins the game.

<table class="table table-striped table-hover" style="font-size: 12px; margin-left: auto; margin-right: auto;">
<caption style="font-size: initial !important;">Win Probability (%)</caption>
 <thead>
<tr>
<th style="border-bottom:hidden" colspan="3"></th>
<th style="border-bottom:hidden; padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; " colspan="9"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Run Differential</div></th>
</tr>
  <tr>
   <th style="text-align:center;"> Inning </th>
   <th style="text-align:center;"> Outs </th>
   <th style="text-align:center;"> Half </th>
   <th style="text-align:center;"> -4+ </th>
   <th style="text-align:center;"> -3 </th>
   <th style="text-align:center;"> -2 </th>
   <th style="text-align:center;"> -1 </th>
   <th style="text-align:center;"> 0 </th>
   <th style="text-align:center;"> 1 </th>
   <th style="text-align:center;"> 2 </th>
   <th style="text-align:center;"> 3 </th>
   <th style="text-align:center;"> 4+ </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.20 </td>
   <td style="text-align:center;"> 0.25 </td>
   <td style="text-align:center;"> 0.18 </td>
   <td style="text-align:center;"> 0.19 </td>
   <td style="text-align:center;"> 0.47 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.25 </td>
   <td style="text-align:center;"> 0.18 </td>
   <td style="text-align:center;"> 0.33 </td>
   <td style="text-align:center;"> 0.49 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.16 </td>
   <td style="text-align:center;"> 0.17 </td>
   <td style="text-align:center;"> 0.38 </td>
   <td style="text-align:center;"> 0.36 </td>
   <td style="text-align:center;"> 0.51 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.16 </td>
   <td style="text-align:center;"> 0.32 </td>
   <td style="text-align:center;"> 0.41 </td>
   <td style="text-align:center;"> 0.37 </td>
   <td style="text-align:center;"> 0.53 </td>
   <td style="text-align:center;"> 0.76 </td>
   <td style="text-align:center;"> 0.80 </td>
   <td style="text-align:center;"> 0.83 </td>
   <td style="text-align:center;"> 0.80 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.13 </td>
   <td style="text-align:center;"> 0.24 </td>
   <td style="text-align:center;"> 0.40 </td>
   <td style="text-align:center;"> 0.37 </td>
   <td style="text-align:center;"> 0.51 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 0.94 </td>
   <td style="text-align:center;"> 0.92 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.09 </td>
   <td style="text-align:center;"> 0.05 </td>
   <td style="text-align:center;"> 0.33 </td>
   <td style="text-align:center;"> 0.32 </td>
   <td style="text-align:center;"> 0.49 </td>
   <td style="text-align:center;"> 0.65 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.92 </td>
   <td style="text-align:center;"> 1.00 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.09 </td>
   <td style="text-align:center;"> 0.05 </td>
   <td style="text-align:center;"> 0.25 </td>
   <td style="text-align:center;"> 0.32 </td>
   <td style="text-align:center;"> 0.46 </td>
   <td style="text-align:center;"> 0.63 </td>
   <td style="text-align:center;"> 0.50 </td>
   <td style="text-align:center;"> 0.89 </td>
   <td style="text-align:center;"> 0.96 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.06 </td>
   <td style="text-align:center;"> 0.12 </td>
   <td style="text-align:center;"> 0.26 </td>
   <td style="text-align:center;"> 0.32 </td>
   <td style="text-align:center;"> 0.45 </td>
   <td style="text-align:center;"> 0.63 </td>
   <td style="text-align:center;"> 0.55 </td>
   <td style="text-align:center;"> 0.94 </td>
   <td style="text-align:center;"> 0.96 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.07 </td>
   <td style="text-align:center;"> 0.19 </td>
   <td style="text-align:center;"> 0.29 </td>
   <td style="text-align:center;"> 0.38 </td>
   <td style="text-align:center;"> 0.49 </td>
   <td style="text-align:center;"> 0.62 </td>
   <td style="text-align:center;"> 0.58 </td>
   <td style="text-align:center;"> 0.93 </td>
   <td style="text-align:center;"> 0.95 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.06 </td>
   <td style="text-align:center;"> 0.29 </td>
   <td style="text-align:center;"> 0.33 </td>
   <td style="text-align:center;"> 0.39 </td>
   <td style="text-align:center;"> 0.50 </td>
   <td style="text-align:center;"> 0.67 </td>
   <td style="text-align:center;"> 0.60 </td>
   <td style="text-align:center;"> 0.96 </td>
   <td style="text-align:center;"> 0.96 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.08 </td>
   <td style="text-align:center;"> 0.27 </td>
   <td style="text-align:center;"> 0.31 </td>
   <td style="text-align:center;"> 0.41 </td>
   <td style="text-align:center;"> 0.51 </td>
   <td style="text-align:center;"> 0.63 </td>
   <td style="text-align:center;"> 0.65 </td>
   <td style="text-align:center;"> 0.89 </td>
   <td style="text-align:center;"> 0.95 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.10 </td>
   <td style="text-align:center;"> 0.22 </td>
   <td style="text-align:center;"> 0.31 </td>
   <td style="text-align:center;"> 0.37 </td>
   <td style="text-align:center;"> 0.47 </td>
   <td style="text-align:center;"> 0.60 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 0.74 </td>
   <td style="text-align:center;"> 0.91 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 0.16 </td>
   <td style="text-align:center;"> 0.31 </td>
   <td style="text-align:center;"> 0.33 </td>
   <td style="text-align:center;"> 0.46 </td>
   <td style="text-align:center;"> 0.58 </td>
   <td style="text-align:center;"> 0.60 </td>
   <td style="text-align:center;"> 0.73 </td>
   <td style="text-align:center;"> 0.91 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 0.14 </td>
   <td style="text-align:center;"> 0.29 </td>
   <td style="text-align:center;"> 0.33 </td>
   <td style="text-align:center;"> 0.47 </td>
   <td style="text-align:center;"> 0.58 </td>
   <td style="text-align:center;"> 0.62 </td>
   <td style="text-align:center;"> 0.79 </td>
   <td style="text-align:center;"> 0.92 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.04 </td>
   <td style="text-align:center;"> 0.18 </td>
   <td style="text-align:center;"> 0.36 </td>
   <td style="text-align:center;"> 0.40 </td>
   <td style="text-align:center;"> 0.45 </td>
   <td style="text-align:center;"> 0.58 </td>
   <td style="text-align:center;"> 0.76 </td>
   <td style="text-align:center;"> 0.77 </td>
   <td style="text-align:center;"> 0.92 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.05 </td>
   <td style="text-align:center;"> 0.16 </td>
   <td style="text-align:center;"> 0.37 </td>
   <td style="text-align:center;"> 0.45 </td>
   <td style="text-align:center;"> 0.49 </td>
   <td style="text-align:center;"> 0.62 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.96 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.04 </td>
   <td style="text-align:center;"> 0.16 </td>
   <td style="text-align:center;"> 0.37 </td>
   <td style="text-align:center;"> 0.43 </td>
   <td style="text-align:center;"> 0.49 </td>
   <td style="text-align:center;"> 0.65 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.84 </td>
   <td style="text-align:center;"> 0.94 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 0.09 </td>
   <td style="text-align:center;"> 0.30 </td>
   <td style="text-align:center;"> 0.39 </td>
   <td style="text-align:center;"> 0.43 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 0.67 </td>
   <td style="text-align:center;"> 0.83 </td>
   <td style="text-align:center;"> 0.91 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.04 </td>
   <td style="text-align:center;"> 0.12 </td>
   <td style="text-align:center;"> 0.26 </td>
   <td style="text-align:center;"> 0.31 </td>
   <td style="text-align:center;"> 0.39 </td>
   <td style="text-align:center;"> 0.61 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.92 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.04 </td>
   <td style="text-align:center;"> 0.16 </td>
   <td style="text-align:center;"> 0.22 </td>
   <td style="text-align:center;"> 0.30 </td>
   <td style="text-align:center;"> 0.41 </td>
   <td style="text-align:center;"> 0.61 </td>
   <td style="text-align:center;"> 0.71 </td>
   <td style="text-align:center;"> 0.83 </td>
   <td style="text-align:center;"> 0.92 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.03 </td>
   <td style="text-align:center;"> 0.19 </td>
   <td style="text-align:center;"> 0.23 </td>
   <td style="text-align:center;"> 0.33 </td>
   <td style="text-align:center;"> 0.44 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 0.77 </td>
   <td style="text-align:center;"> 0.83 </td>
   <td style="text-align:center;"> 0.91 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.05 </td>
   <td style="text-align:center;"> 0.21 </td>
   <td style="text-align:center;"> 0.22 </td>
   <td style="text-align:center;"> 0.36 </td>
   <td style="text-align:center;"> 0.50 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 0.79 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 0.92 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.05 </td>
   <td style="text-align:center;"> 0.21 </td>
   <td style="text-align:center;"> 0.18 </td>
   <td style="text-align:center;"> 0.38 </td>
   <td style="text-align:center;"> 0.53 </td>
   <td style="text-align:center;"> 0.60 </td>
   <td style="text-align:center;"> 0.78 </td>
   <td style="text-align:center;"> 0.80 </td>
   <td style="text-align:center;"> 0.92 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.06 </td>
   <td style="text-align:center;"> 0.23 </td>
   <td style="text-align:center;"> 0.18 </td>
   <td style="text-align:center;"> 0.30 </td>
   <td style="text-align:center;"> 0.46 </td>
   <td style="text-align:center;"> 0.60 </td>
   <td style="text-align:center;"> 0.71 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.92 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.03 </td>
   <td style="text-align:center;"> 0.20 </td>
   <td style="text-align:center;"> 0.14 </td>
   <td style="text-align:center;"> 0.29 </td>
   <td style="text-align:center;"> 0.41 </td>
   <td style="text-align:center;"> 0.58 </td>
   <td style="text-align:center;"> 0.66 </td>
   <td style="text-align:center;"> 0.80 </td>
   <td style="text-align:center;"> 0.93 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.05 </td>
   <td style="text-align:center;"> 0.19 </td>
   <td style="text-align:center;"> 0.19 </td>
   <td style="text-align:center;"> 0.30 </td>
   <td style="text-align:center;"> 0.45 </td>
   <td style="text-align:center;"> 0.59 </td>
   <td style="text-align:center;"> 0.69 </td>
   <td style="text-align:center;"> 0.77 </td>
   <td style="text-align:center;"> 0.92 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.06 </td>
   <td style="text-align:center;"> 0.23 </td>
   <td style="text-align:center;"> 0.16 </td>
   <td style="text-align:center;"> 0.35 </td>
   <td style="text-align:center;"> 0.45 </td>
   <td style="text-align:center;"> 0.60 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 0.85 </td>
   <td style="text-align:center;"> 0.95 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.06 </td>
   <td style="text-align:center;"> 0.25 </td>
   <td style="text-align:center;"> 0.20 </td>
   <td style="text-align:center;"> 0.38 </td>
   <td style="text-align:center;"> 0.49 </td>
   <td style="text-align:center;"> 0.60 </td>
   <td style="text-align:center;"> 0.82 </td>
   <td style="text-align:center;"> 0.85 </td>
   <td style="text-align:center;"> 0.96 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.06 </td>
   <td style="text-align:center;"> 0.21 </td>
   <td style="text-align:center;"> 0.18 </td>
   <td style="text-align:center;"> 0.38 </td>
   <td style="text-align:center;"> 0.52 </td>
   <td style="text-align:center;"> 0.59 </td>
   <td style="text-align:center;"> 0.80 </td>
   <td style="text-align:center;"> 0.86 </td>
   <td style="text-align:center;"> 0.96 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.05 </td>
   <td style="text-align:center;"> 0.21 </td>
   <td style="text-align:center;"> 0.15 </td>
   <td style="text-align:center;"> 0.27 </td>
   <td style="text-align:center;"> 0.50 </td>
   <td style="text-align:center;"> 0.58 </td>
   <td style="text-align:center;"> 0.72 </td>
   <td style="text-align:center;"> 0.83 </td>
   <td style="text-align:center;"> 0.95 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.03 </td>
   <td style="text-align:center;"> 0.15 </td>
   <td style="text-align:center;"> 0.12 </td>
   <td style="text-align:center;"> 0.23 </td>
   <td style="text-align:center;"> 0.43 </td>
   <td style="text-align:center;"> 0.56 </td>
   <td style="text-align:center;"> 0.67 </td>
   <td style="text-align:center;"> 0.80 </td>
   <td style="text-align:center;"> 0.96 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 0.15 </td>
   <td style="text-align:center;"> 0.12 </td>
   <td style="text-align:center;"> 0.24 </td>
   <td style="text-align:center;"> 0.45 </td>
   <td style="text-align:center;"> 0.53 </td>
   <td style="text-align:center;"> 0.71 </td>
   <td style="text-align:center;"> 0.83 </td>
   <td style="text-align:center;"> 0.96 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.04 </td>
   <td style="text-align:center;"> 0.13 </td>
   <td style="text-align:center;"> 0.16 </td>
   <td style="text-align:center;"> 0.25 </td>
   <td style="text-align:center;"> 0.44 </td>
   <td style="text-align:center;"> 0.55 </td>
   <td style="text-align:center;"> 0.76 </td>
   <td style="text-align:center;"> 0.85 </td>
   <td style="text-align:center;"> 0.98 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.03 </td>
   <td style="text-align:center;"> 0.19 </td>
   <td style="text-align:center;"> 0.17 </td>
   <td style="text-align:center;"> 0.28 </td>
   <td style="text-align:center;"> 0.47 </td>
   <td style="text-align:center;"> 0.61 </td>
   <td style="text-align:center;"> 0.86 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 0.99 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 0.16 </td>
   <td style="text-align:center;"> 0.21 </td>
   <td style="text-align:center;"> 0.24 </td>
   <td style="text-align:center;"> 0.49 </td>
   <td style="text-align:center;"> 0.65 </td>
   <td style="text-align:center;"> 0.82 </td>
   <td style="text-align:center;"> 0.82 </td>
   <td style="text-align:center;"> 0.98 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 0.11 </td>
   <td style="text-align:center;"> 0.13 </td>
   <td style="text-align:center;"> 0.19 </td>
   <td style="text-align:center;"> 0.45 </td>
   <td style="text-align:center;"> 0.55 </td>
   <td style="text-align:center;"> 0.82 </td>
   <td style="text-align:center;"> 0.87 </td>
   <td style="text-align:center;"> 0.98 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 0.06 </td>
   <td style="text-align:center;"> 0.09 </td>
   <td style="text-align:center;"> 0.10 </td>
   <td style="text-align:center;"> 0.34 </td>
   <td style="text-align:center;"> 0.54 </td>
   <td style="text-align:center;"> 0.76 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.97 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 0.06 </td>
   <td style="text-align:center;"> 0.08 </td>
   <td style="text-align:center;"> 0.11 </td>
   <td style="text-align:center;"> 0.32 </td>
   <td style="text-align:center;"> 0.55 </td>
   <td style="text-align:center;"> 0.81 </td>
   <td style="text-align:center;"> 0.84 </td>
   <td style="text-align:center;"> 0.98 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.03 </td>
   <td style="text-align:center;"> 0.07 </td>
   <td style="text-align:center;"> 0.09 </td>
   <td style="text-align:center;"> 0.14 </td>
   <td style="text-align:center;"> 0.31 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 0.77 </td>
   <td style="text-align:center;"> 0.91 </td>
   <td style="text-align:center;"> 0.99 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.03 </td>
   <td style="text-align:center;"> 0.08 </td>
   <td style="text-align:center;"> 0.13 </td>
   <td style="text-align:center;"> 0.16 </td>
   <td style="text-align:center;"> 0.34 </td>
   <td style="text-align:center;"> 0.68 </td>
   <td style="text-align:center;"> 0.85 </td>
   <td style="text-align:center;"> 0.95 </td>
   <td style="text-align:center;"> 0.98 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 0.06 </td>
   <td style="text-align:center;"> 0.15 </td>
   <td style="text-align:center;"> 0.19 </td>
   <td style="text-align:center;"> 0.34 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 0.86 </td>
   <td style="text-align:center;"> 0.96 </td>
   <td style="text-align:center;"> 0.98 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.01 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.08 </td>
   <td style="text-align:center;"> 0.10 </td>
   <td style="text-align:center;"> 0.24 </td>
   <td style="text-align:center;"> 0.62 </td>
   <td style="text-align:center;"> 0.82 </td>
   <td style="text-align:center;"> 0.95 </td>
   <td style="text-align:center;"> 0.99 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.01 </td>
   <td style="text-align:center;"> 0.03 </td>
   <td style="text-align:center;"> 0.08 </td>
   <td style="text-align:center;"> 0.12 </td>
   <td style="text-align:center;"> 0.19 </td>
   <td style="text-align:center;"> 0.59 </td>
   <td style="text-align:center;"> 0.70 </td>
   <td style="text-align:center;"> 0.88 </td>
   <td style="text-align:center;"> 0.98 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.01 </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 0.07 </td>
   <td style="text-align:center;"> 0.11 </td>
   <td style="text-align:center;"> 0.20 </td>
   <td style="text-align:center;"> 0.58 </td>
   <td style="text-align:center;"> 0.84 </td>
   <td style="text-align:center;"> 0.97 </td>
   <td style="text-align:center;"> 1.00 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.01 </td>
   <td style="text-align:center;"> 0.03 </td>
   <td style="text-align:center;"> 0.08 </td>
   <td style="text-align:center;"> 0.09 </td>
   <td style="text-align:center;"> 0.24 </td>
   <td style="text-align:center;"> 0.64 </td>
   <td style="text-align:center;"> 0.85 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 1.00 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.01 </td>
   <td style="text-align:center;"> 0.05 </td>
   <td style="text-align:center;"> 0.08 </td>
   <td style="text-align:center;"> 0.16 </td>
   <td style="text-align:center;"> 0.25 </td>
   <td style="text-align:center;"> 0.78 </td>
   <td style="text-align:center;"> 0.94 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 1.00 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.01 </td>
   <td style="text-align:center;"> 0.08 </td>
   <td style="text-align:center;"> 0.06 </td>
   <td style="text-align:center;"> 0.07 </td>
   <td style="text-align:center;"> 0.25 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.93 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 1.00 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.12 </td>
   <td style="text-align:center;"> 0.07 </td>
   <td style="text-align:center;"> 0.23 </td>
   <td style="text-align:center;"> 0.80 </td>
   <td style="text-align:center;"> 0.92 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 1.00 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 0.75 </td>
   <td style="text-align:center;"> 0.84 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 1.00 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 0.89 </td>
   <td style="text-align:center;"> 0.91 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 1.00 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 0.92 </td>
   <td style="text-align:center;"> 0.97 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 1.00 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 0.50 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 1.00 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 1.00 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.02 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 1.00 </td>
   <td style="text-align:center;"> 1.00 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 11 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 11 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 11 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 11 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 11 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 11 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 12 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 12 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 12 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 12 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 12 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 12 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 13 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 13 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 13 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> top </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 13 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 13 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 13 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> bottom </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> 0.00 </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
   <td style="text-align:center;"> NA </td>
  </tr>
</tbody>
</table>

All probabilities are for the home team winning the game. If the home team gives up a first inning run before making an out, the win probability drops from 47% to 19% or a 28% decline. This chart, combined with the other run scoring information, can be used to make in-game decisions that help increase run expectancy and ultimately win probability. 
