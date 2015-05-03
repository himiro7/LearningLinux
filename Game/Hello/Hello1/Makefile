
#プログラム名とオブジェクトファイル名
PROGRAM = hello1.out
OBJS = hello1.o
LIBS = /usr/lib/x86_64-linux-gnu/libncurses.so
#LDLIBS = -L/usr/lib/x86_64-linux-gnu

#マクロ再定義
CC = gcc
#CFLAGS = ??

#サフィックスルール適応対象の拡張子の定義
.SUFFIXES: .c .o

#プライマリーターゲット
$(PROGRAM): $(OBJS)
	$(CC) -o $(PROGRAM) $^ $(LIBS)

#サフィックスルール
.c.o:
	$(CC) $(CFLAGS) -c $<

#生成ファイル削除用ダミーターゲット
.PHONY: clean
clean:
	$(RM) $(PROGRAM) $(OBJS)

#ヘッダファイルの依存関係
#hello1.o: xxx.h
