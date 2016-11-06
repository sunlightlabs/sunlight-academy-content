<h1>Setting Up Datajam</h1>

Learn how to install and configure our award-winning real-time reporting platform, Datajam. It's the platform that powers our own Sunlight Live and can enable real-time reporting, context and analysis on your site quickly, easily and cheaply.
Datajam is a real-time reporting platform created by the Sunlight Foundation. The concept of Datajam is to simplify reporting live events in real time with a focus on displaying contextual data and information in accessible ways.

We call our implementation <a href="http://sunlightlive.com">Sunlight Live</a>, but the underlying platform is called Datajam and has been made <a href="https://github.com/sunlightlabs/datajam/">freely available</a> to the public.

There are three basic components to the Datajam platform:
<ul>
<li><b>Live video stream:</b> To embed video into the platform, simply paste video embed code into this module.</li>
<li><b>Real-time chat:</b> With connections to social networks and URL shorteners, this chat module was built by Sunlight Labs from the ground up. It includes a comment moderation interface to keep conversations civil and on track.</li>
<li><b>Contextual data cards:</b> Our datacard system makes it easy for hosts to create contextual data cards featuring tables, charts and graphs. Included with Datajam is a plugin to connect automatically to our Influence Explorer site.</li>
</ul>

So, let's walk through installing Datajam for your own use.

We built Datajam as a Ruby on Rails application that can be deployed in any number of ways. We think the easiest is through the <a href="heroku.com">Heroku</a> cloud-based application hosting environment. For the purposes of this module, that's the setup we're going to assume.

There are two pieces of software that must first be installed on your computer before you can continue. They are Ruby and Git. You can get more information about each and how to install them here:

Mac: <a href="http://mxcl.github.com/homebrew/">Ruby</a> | <a href="http://code.google.com/p/git-osx-installer">Git</a>
Linux: <a href="http://www.ruby-lang.org/en/downloads/">Ruby</a> | <a href="http://git-scm.com/book/en/Getting-Started-Installing-Git">Git</a>
Windows: <a href="http://rubyinstaller.org/">Ruby</a> | <a href="http://code.google.com/p/msysgit">Git</a>

<h3>My Heroku</h3>

<p>Once you've set up your local machine with Ruby and Git, you&#8217;ll next need to sign up for a free Heroku account. Sign up at <a href="https://api.heroku.com/signup">https://api.heroku.com/signup</a>.</p> Heroku has <a href="http://www.heroku.com/pricing#0-0">various service levels</a>, including basic service that is free and would be sufficient for running small Datajam events. As your events grow, Heroku can scale services accordingly at pretty low rates. Even heavy Datajam users should expect Heroku charges to be less than $10/month.

<p>Once you are set up with Heroku, read through Heroku&#8217;s <a href="http://devcenter.heroku.com/articles/quickstart">Quickstart Guide</a> to get setup with their tool belt. You need only go through step 3 for our purposes.</p>

<h3>Git the code</h3>

Now that you've set up your machine with Ruby and Git, and gotten your Heroku account, it's time to download Datajam. We maintain and distribute Datajam's code through GitHub. And in order to move the code from GitHub to your Heroku instance, you must first download the code to your local machine.

There are a number of steps involved in this process, so we've simplified it with one simple shell command:

<code>sh <(curl http://get.datajam.org)</code>

When you run the above command in Terminal, you will be prompted to name the application. Then the script will:

<ul>
<li>download the repository from GitHub</li>
<li>create a blank Heroku application</li>
<li>install Datajam's software dependencies, such as Ruby on Rails</li>
<li>deploy the application to Heroku<li>
<li>initialize a database with a default template and admin user account</li>
</ul>

When the script is finished, you will be given a URL where the code has been installed, along with a username and password. Go ahead and log in to see what you've created.

<h3>Configuration</h3>

With Datajam installed, it's time to start configuring it for your site. The first step in this process is to manage the templates. We will walk you through the basics of this, but the specifics of your template design will depend on your needs. For example, some users might want to design their installation of Datajam so that it looks just like their website.
