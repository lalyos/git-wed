## initialize

create dir
```
mkdir git-wed
cd git-wed
```

create repo
```
git init
```

## Create first file

```
echo 'echo gimme coffee' > coffee.sh
chmod 755 coffee.sh
```

stage new file
```
git add coffee.sh
```

create first commit:
```
git commit -m "coffee added"
```

## 2. commit

```
echo 'echo gimme milk' >> coffee.sh
```

```
git commit -am "milk added"
```

## 3.commit


```
echo 'echo gimme 2 sugars' >> coffee.sh
```

```
git commit -am "sugar added"
```

## tag

```
git tag v1.0
```

## Simulate changes on master (somebody else)

```
echo 'echo lets go lunch' > lunch.sh
chmod 755 lunch.sh
```

```
git add lunch.sh
git commit -m "lunch added"
```

```
echo 'echo gimme pacal' >> lunch.sh 
git commit -am "pacal ordered"
```

## start feature-branch

```
git checkout -b fix v1.0
sed -i.bak 's/gimme/give me/' coffee.sh
git commit -am "typo fixed"
```

new commit
```
sed -i.bak 's/2/3/' coffee.sh
git commit -am "one more sugar"
```
