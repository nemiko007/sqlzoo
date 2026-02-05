# STRONGLY AGREEの割合を表示

**テーブル構造:** `nss(ukprn, institution, subject, level, question, response, sample, score, A_STRONGLY_DISAGREE, A_DISAGREE, A_NEUTRAL, A_AGREE, A_STRONGLY_AGREE)`

Edinburgh Napier Universityで(8) Computer Scienceを専攻している学生のQ01への回答を表示
```sql
SELECT A_STRONGLY_AGREE FROM nss 
WHERE question='Q01' 
  AND institution='Edinburgh Napier University' 
  AND subject='(8) Computer Science'
```
