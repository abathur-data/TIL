# MySQL String, Date 관련 함수

## String 관련 함수

| 함수                                 | 설명                       | 예시                                                |
| ------------------------------------ | -------------------------- | --------------------------------------------------- |
| `CONCAT(s1, s2, ...)`                | 문자열 합치기              | `CONCAT('Hello', ' ', 'World') → 'Hello World'`     |
| `SUBSTRING(str, pos, len)`           | 부분 문자열 추출           | `SUBSTRING('abcdef', 2, 3) → 'bcd'`                 |
| `LEFT(str, len)` / `RIGHT(str, len)` | 왼쪽/오른쪽에서 n글자      | `LEFT('abcdef', 2) → 'ab'`                          |
| `LENGTH(str)` / `CHAR_LENGTH(str)`   | 바이트 수 / 문자 수        | `LENGTH('가나다') → 6`, `CHAR_LENGTH('가나다') → 3` |
| `REPLACE(str, from, to)`             | 문자열 치환                | `REPLACE('abcabc', 'a', 'x') → 'xbcxbc'`            |
| `TRIM(str)` / `LTRIM()` / `RTRIM()`  | 공백 제거                  | `TRIM('  hi  ') → 'hi'`                             |
| `LOWER(str)` / `UPPER(str)`          | 소문자 / 대문자 변환       | `LOWER('ABC') → 'abc'`                              |
| `INSTR(str, substr)`                 | 부분 문자열 위치           | `INSTR('abcabc', 'b') → 2`                          |
| `REVERSE(str)`                       | 문자열 뒤집기              | `REVERSE('abc') → 'cba'`                            |
| `FORMAT(number, decimals)`           | 숫자에 천 단위 쉼표 붙이기 | `FORMAT(1234567.89, 2) → '1,234,567.89'`            |

## Date/Time 관련 함수

| 함수                               | 설명                   | 예시                                                         |
| ---------------------------------- | ---------------------- | ------------------------------------------------------------ |
| `NOW()`                            | 현재 날짜 및 시간      | `2025-04-09 14:30:00`                                        |
| `CURDATE()` / `CURTIME()`          | 현재 날짜 / 시간       | `CURDATE() → 2025-04-09`                                     |
| `DATE()`                           | datetime에서 날짜만    | `DATE(NOW()) → 2025-04-09`                                   |
| `YEAR()` / `MONTH()` / `DAY()`     | 날짜의 연, 월, 일 추출 | `YEAR('2024-09-01') → 2024`                                  |
| `HOUR()` / `MINUTE()` / `SECOND()` | 시간 요소 추출         | `HOUR('14:25:10') → 14`                                      |
| `DATEDIFF(d1, d2)`                 | 두 날짜 차이 (일 단위) | `DATEDIFF('2025-04-09', '2025-04-01') → 8`                   |
| `TIMESTAMPDIFF(unit, d1, d2)`      | 단위별 날짜 차이       | `TIMESTAMPDIFF(HOUR, '2025-04-01 12:00', '2025-04-02 12:00') → 24` |
| `DATE_ADD(date, INTERVAL n unit)`  | 날짜 더하기            | `DATE_ADD('2025-04-01', INTERVAL 3 DAY) → '2025-04-04'`      |
| `DATE_SUB(date, INTERVAL n unit)`  | 날짜 빼기              | `DATE_SUB('2025-04-01', INTERVAL 1 MONTH) → '2025-03-01'`    |
| `STR_TO_DATE(str, format)`         | 문자열 → 날짜 변환     | `STR_TO_DATE('2025-04-09', '%Y-%m-%d')`                      |
| `DATE_FORMAT(date, format)`        | 날짜 → 문자열 형식화   | `DATE_FORMAT(NOW(), '%Y-%m-%d %H:%i')`                       |