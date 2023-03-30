# merge commit of b

## git show

```bash
$ git show HEAD
commit 4351a35ca172efe033cb774a7fb8daa885f25f16 (HEAD -> master)
Merge: 5566823 ddd44dc
Author: me
Date:   Thu Mar 30 08:10:20 2023 +0200

    Merge branch 'b'

    # Conflicts:
    #       foo.txt

diff --cc foo.txt
```

```diff
index 2b4cd2b,011c698..98f128b
--- a/foo.txt
+++ b/foo.txt
@@@ -47,7 -47,7 +47,7 @@@
  47
  48
  49
- 42
 -4711
++123456789
  51
  52
  53

```

## git diff (like SM)


```diff
git diff HEAD^ HEAD
diff --git a/foo.txt b/foo.txt
index 2b4cd2b..98f128b 100644
--- a/foo.txt
+++ b/foo.txt
@@ -47,7 +47,7 @@
 47
 48
 49
-42
+123456789
 51
 52
 53
@@ -87,8 +87,8 @@
 87
 88
 89
-90
-91
+900
+910
 92
 93
 94
@@ -96,5 +96,5 @@
 96
 97
 98
-99
-100
\ No newline at end of file
+990
+1000
\ No newline at end of file


```

# merge commit of a


## git show


```bash
git show HEAD^
commit 5566823f36ec3e4b77a746d3308edaa7e08fe1a6
Merge: 475b83c 5f90cd5
Author: me
Date:   Thu Mar 30 08:09:25 2023 +0200

    Merge branch 'a'

    # Conflicts:
    #       foo.txt

diff --cc foo.txt
```

```diff
index cffa327,f2c7778..2b4cd2b
--- a/foo.txt
+++ b/foo.txt
@@@ -47,7 -47,7 +47,7 @@@
  47
  48
  49
- 500
 -1620
++42
  51
  52

```

## git diff (like SM)

```diff
git diff HEAD^^ HEAD^
diff --git a/foo.txt b/foo.txt
index cffa327..2b4cd2b 100644
--- a/foo.txt
+++ b/foo.txt
@@ -1,13 +1,13 @@
-1
-2
+10
+20
 3
 4
 5
 6
 7
 8
-9
-10
+90
+100
 11
 12
 13
@@ -47,7 +47,7 @@
 47
 48
 49
-500
+42
 51
 52
 53

```
