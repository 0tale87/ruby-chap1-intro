# テクノロジー（藤原） 授業 6/8

今日の授業で打ったコマンドをコピー＆ペーストしてください。

（`irb`や`ruby`の実行結果も含めて全てをコピーしてください）

## ターミナルに打ったコマンド

```
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ irb
irb(main):001:0> print("Hello,Ruby.\n")
Hello,Ruby.
=> nil
irb(main):002:0> 1+1
=> 2
irb(main):003:0> "Hello,Ruby.\n"
=> "Hello,Ruby.\n"
irb(main):004:0> "Hello,Ruby.\n"class
Traceback (most recent call last):
        1: from /Users/rei/.rbenv/versions/2.5.1/bin/irb:11:in `<main>'
SyntaxError ((irb):4: syntax error, unexpected keyword_class, expecting end-of-input)
"Hello,Ruby.\n"class
               ^~~~~
irb(main):005:0> "Hello,Ruby.\n".class
=> String
irb(main):006:0> 1+1.class
Traceback (most recent call last):
        3: from /Users/rei/.rbenv/versions/2.5.1/bin/irb:11:in `<main>'
        2: from (irb):6
        1: from (irb):6:in `+'
TypeError (Class can't be coerced into Integer)
irb(main):007:0> (1+1).class
=> Integer
irb(main):008:0> irb --simple-prompt
Traceback (most recent call last):
        2: from /Users/rei/.rbenv/versions/2.5.1/bin/irb:11:in `<main>'
        1: from (irb):8
NameError (undefined local variable or method `simple' for main:Object)
irb(main):009:0> irb --simple-promp
Traceback (most recent call last):
        2: from /Users/rei/.rbenv/versions/2.5.1/bin/irb:11:in `<main>'
        1: from (irb):9
NameError (undefined local variable or method `simple' for main:Object)
irb(main):010:0>
maesakareinoMacBook-Pro:ruby-chap1-intro rei$
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ irb --simple-prompt
>> 1+1
=> 2
>> 2-1
=> 1
>> 2-3
=> -1
>> 5*10
=> 50
>> 100/4
=> 25
>> 1.class
=> Integer
>> 3.1415
=> 3.1415
>> (3.1415).class
=> Float
>> print("表面積=",area,"\n")
Traceback (most recent call last):
        2: from /Users/rei/.rbenv/versions/2.5.1/bin/irb:11:in `<main>'
        1: from (irb):9
NameError (undefined local variable or method `area' for main:Object)
>> print"表面積=",area,"\n"
Traceback (most recent call last):
        2: from /Users/rei/.rbenv/versions/2.5.1/bin/irb:11:in `<main>'
        1: from (irb):10
NameError (undefined local variable or method `area' for main:Object)
>> print "表面積=",area,"\n"
Traceback (most recent call last):
        2: from /Users/rei/.rbenv/versions/2.5.1/bin/irb:11:in `<main>'
        1: from (irb):11
NameError (undefined local variable or method `area' for main:Object)
>> print"Hello,Ruby.\n"
Hello,Ruby.
=> nil
>>
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ irb
irb(main):001:0> print "Hello,","Ruby",".","\n"
Hello,Ruby.
=> nil
irb(main):002:0>
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ irb --simple-prompt
>> puts(10)
10
=> nil
>> math(sin1)
Traceback (most recent call last):
        2: from /Users/rei/.rbenv/versions/2.5.1/bin/irb:11:in `<main>'
        1: from (irb):2
NameError (undefined local variable or method `sin1' for main:Object)
>> math.sin(1)
Traceback (most recent call last):
        2: from /Users/rei/.rbenv/versions/2.5.1/bin/irb:11:in `<main>'
        1: from (irb):3
NameError (undefined local variable or method `math' for main:Object)
>> Math.sin(1)
=> 0.8414709848078965
>> Math.sin(3.14)
=> 0.0015926529164868282
>> x=10
=> 10
>> y=20
=> 20
>> z=30
=> 30
>> area=(x*y+y*z+z*x)*2
=> 2200
>> volume=(x+y+z)
=> 60
>> volume=(x*y*z)
=> 6000
>> print("表面積=",area,"\n")
表面積=2200
=> nil
>> print("体積=",volume,"\n")
体積=6000
=> nil
>> print("表面積=#{area}\n")
表面積=2200
=> nil
>> puts("表面積=#{area}")
表面積=2200
=> nil
>> print ("表面積=#{area}")
表面積=2200=> nil
>> puts ("Hello,Ruby.")
Hello,Ruby.
=> nil
>>
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ ls
README.md	helloruby.rb	puts_and_p
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ ls
README.md	helloruby.rb	puts_and_p.rb
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ ruby puts_and_p.rb
Hello,
	Ruby.
"Hello,\n\tRuby"
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ ls
README.md	helloruby.rb	puts_and_p.rb
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ ls
README.md	helloruby.rb	kiritsubo.rb	puts_and_p.rb
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ ruby kiritubo.rb
Traceback (most recent call last):
ruby: No such file or directory -- kiritubo.rb (LoadError)
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ ruby kiritsubo.rb
いづれの御時にか女御更衣あまたさぶらいたまいけるなかに
いとやむごとなき際にはあらぬがすぐれて時めきたまふありけり
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ ls
README.md	area_volume.rb	helloruby.rb	kiritsubo.rb	puts_and_p.rb
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ ruby area_volume
Traceback (most recent call last):
ruby: No such file or directory -- area_volume (LoadError)
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ ruby area_volume.rb
表面積=x*y+y*z+z*xx*y+y*z+z*x
体積=6000
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ ruby area_volume.rb
表面積=2200
体積=6000
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ ruby comment_sample.rb
表面積=2200
体積=6000
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ ruby greater_smaller.rb
greater
maesakareinoMacBook-Pro:ruby-chap1-intro rei$ ruby greater_smaller_else.rb
greater

```
