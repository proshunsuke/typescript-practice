# 2

react

## setup

```bash
make clean
make setup
make run
```

## 備考

dockerコンテナ内でmy-appを作成しているので、作成したファイルの所有権がrootになってしまっている。ファイルを編集するためには以下を実行

```bash
make change-owner 
```

## 参考

[TypeScript React Starter](https://github.com/Microsoft/TypeScript-React-Starter#typescript-react-starter)
