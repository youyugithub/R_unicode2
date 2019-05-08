# R_unicode2
R unicode2

http://bmb-common.blogspot.com/2011/05/unicode-symbols-in-r.html

```
TestUnicode <- function(start="25a0", end="25ff", ...)
  {
    nstart <- as.hexmode(start)
    nend <- as.hexmode(end)
    r <- nstart:nend
    s <- ceiling(sqrt(length(r)))
    par(pty="s")
    plot(c(-1,(s)), c(-1,(s)), type="n", xlab="", ylab="",
         xaxs="i", yaxs="i")
    grid(s+1, s+1, lty=1)
    for(i in seq(r)) {
      try(points(i%%s, i%/%s, pch=-1*r[i],...))
    }
  }

TestUnicode()
TestUnicode(9500,9900)  ## some cool spooky stuff in here!

```
