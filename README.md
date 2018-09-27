

<p>These commands and programs were tried using a zorin os core live usb<br>
your mileage may vary</p>
<h1 id="installing-kotlin">Installing Kotlin</h1>
<p>First we are going to run a command that installs sdkman</p>
<pre><code>curl  -s  https://get.sdkman.io  |  bash
</code></pre>
<p>Active kotlin by</p>
<pre><code>   source "/home/zorin/.sdkman/bin/sdkman-init.sh"
</code></pre>
<p>Next install kotlin</p>
<pre><code> sdk  install  kotlin
</code></pre>
<p><img src="https://preview.ibb.co/nKJuxU/Screenshot_from_2018_09_27_15_21_17.png" alt="Kotlin Program"><br>
hello.kt</p>
<pre><code>   fun main(args: Array&lt;String&gt;) {
        println("Hello, World!")
    }
</code></pre>
<p>Now we test if it works<br>
First we need to compile it to jar file</p>
<pre><code>   kotlinc  hello.kt  -include-runtime  -d  hello.jar
</code></pre>
<p>We get this error</p>
<pre><code> /home/zorin/.sdkman/candidates/kotlin/current/bin/kotlinc: line 74: java: command not found
</code></pre>
<p>We need to install java next</p>
<pre><code>sudo add-apt-repository ppa:webupd8team/java 
sudo apt-get update 
sudo apt-get install
sudo apt install oracle-java8-installer
</code></pre>
<p><img src="https://preview.ibb.co/daRWu9/Screenshot_from_2018_09_27_15_34_13.png" alt="java8-license"><br>
You get presented by this license agreement<br>
Now we run the compilation again</p>
<pre><code>kotlinc hello.kt -include-runtime -d hello.jar
</code></pre>
<p>And</p>
<pre><code>ls 
Desktop    Downloads  hello.kt  Pictures  Templates
Documents  hello.jar  Music     Public    Videos
</code></pre>
<p>There is hello.jar now<br>
We can run it now</p>
<pre><code>  java  -jar  hello.jar
  zorin@zorin:~$ java -jar hello.jar  
  Hello, World!
</code></pre>
<h1 id="installing-ruby">Installing ruby</h1>
<p>We will first install rvm  a ruby version manager<br>
this add those two gpg keys to your local directory</p>
<pre><code>gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
\curl -sSL https://get.rvm.io | bash -s stable --ruby
</code></pre>
<p>Next lets activate ruby</p>
<pre><code>source /home/zorin/.rvm/scripts/rvm
</code></pre>
<p><img src="https://preview.ibb.co/mpvugp/Screenshot_from_2018_09_27_15_48_27.png" alt="ruby program"><br>
Running our code with</p>
<pre><code>ruby helloworld.rb
zorin@zorin:~$ ruby helloworld.rb 
Hello World
</code></pre>
<h2 id="installing-node.js">Installing Node.js</h2>
<p>Next programming language is node.js used in server side programming<br>
this adds the node key and yarn key to your local keys<br>
and updates your repository<br>
and installs them</p>
<pre><code>curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update
sudo apt-get install -y yarn nodejs
</code></pre>
<p>Next we create a basic node app<br>
<img src="https://preview.ibb.co/e7VPE9/Screenshot_from_2018_09_27_16_17_34.png" alt="node app"></p>
<pre><code>zorin@zorin:~$ node app.js 
hello world
</code></pre>
<h2 id="kotlin-console-program">Kotlin Console program</h2>
<pre><code>zorin@zorin:~$ kotlinc input.kt -include-runtime -d input.jar
zorin@zorin:~$ java -jar input.jar
Enter a number20
The output is:120zorin@zorin:~$ 



fun main(args: Array&lt;String&gt;) {
    print("Enter a number")
    var variableName:Int = readLine()!!.toInt()  // readLine() is used to accep$
    var result:Int= variableName*6
    print("The output is:$result")
}
</code></pre>
<p>this takes the number assignes it to variableName:Int and multiplies it by 6 and the result is stored in a variable called result</p>
<h2 id="ruby-console-program">Ruby console program</h2>
<pre><code>
    puts "Enter A"
    a = gets.chomp
    puts "Enter B"
    b = gets.chomp
    c = a.to_i + b.to_i
    puts c
</code></pre>
<p>This puts first input to variable named a.<br>
Second Input to variable named b converst them to an int and adds them together to variable named c</p>
<h2 id="node.js-console-application">Node.js console application</h2>
<p><img src="https://preview.ibb.co/mGuJrp/Screenshot_from_2018_09_27_16_52_33.png" alt="node.js application"><br>
this creates a readline interface<br>
asks a question "What do you think of Node.js? "<br>
and captures input to a variable called answer<br>
i log it to the console adding 5 to it</p>
<h2 id="sources">Sources</h2>
<p><a href="https://kotlinlang.org/docs/tutorials/command-line.html">kotlinlang.org</a><br>
<a href="http://tipsonubuntu.com/2016/07/31/install-oracle-java-8-9-ubuntu-16-04-linux-mint-18/">tipsonubuntu.com</a><br>
<a href="rvm.io">rvm.io</a><br>
<a href="https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions">nodejs.org</a><br>
<a href="https://stackoverflow.com/questions/41283393/reading-console-input-in-kotlin">console kotlin</a><br>
<a href="https://stackoverflow.com/questions/6556280/read-input-from-console-in-ruby">console ruby</a><br>
<a href="https://nodejs.org/api/readline.html">console node.js</a></p>

