+++
date = "2015-03-03T21:39:38-08:00"
draft = false
title = "welcome"
type = "post"

+++

<p>
    <script src="https://gist.github.com/danmux/042fa69bed3791afe658.js">
    </script>
</p>

{{< highlight python >}}
def digit_sum(n):
    s = 0
    while n:   # while n is 'truthy' for an integer that means not 0
        s = s + (n % 10)   # the sum is the sum + the remainder of dividing the incoming number (n) by 10  157 % 10 = 7
        n = n / 10         # n = the integer of n / 10   int(15.7) = 15
    return s

print digit_sum(157)

'''
calling digit_sum(157)

loop  | s   | n   | n % 10  | n / 10
------------------------------------
0     | 0   | 157 |   7     |  15
1     | 7   | 15  |   5     |  1
2     | 12  | 1   |   1     |  0
3     | 13  | 0   |         |
'''
{{< /highlight >}}

{{< highlight html >}}
<section id="main">
  <div>
    <h1 id="title">{{ .Title }}</h1>
    {{ range .Data.Pages }}
        {{ .Render "summary"}}
    {{ end }}
  </div>
</section>
{{< /highlight >}}


