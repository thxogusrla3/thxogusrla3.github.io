---
layout: post
title:  "카카오 비밀지도"
date:   2020-05-29 19:34:36 +0530
categories: Java
---

카카오 비밀지도 문제풀이.

StringBuilder
---

```javascript
class Solution {
    public String[] solution(int n, int[] arr1, int[] arr2) {
        String [] answer = new String[n];
        for (int i = 0; i < n; i++) {
            StringBuilder sb = new StringBuilder(Integer.toBinaryString(arr1[i] | arr2[i]));
            int size = n - sb.length(); //자릿수보다 2진수 값들이 적게 나오면 size 크기만큼 0을 붙임.
            System.out.println("i번째="+i+" " + sb + " sb길이=" + sb.length() + " size="+size);
            for (int j = 0; j < size; j++) {
                sb.insert(0, '0');
                System.out.println(sb);
            }
            answer[i] = sb.toString().replace("1", "#").replace("0", " ");
        }

        return answer;
    }
}
```
StringBuilder 클래스의 append함수는 마지막에 문자열을 추가해주는 함수였습니다.
insert함수는 지정한 위치에 문자열을 추가할 수 있습니다.


[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
