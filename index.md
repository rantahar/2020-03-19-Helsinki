---
layout: workshop      # DON'T CHANGE THIS.
venue: "Kumpula Campus, Exactum CK107"        # brief name of host site without address (e.g., "Euphoric State University")
address: "Exactum CK107, at Gustaf Hällströmin katu 2, 00560 Helsinki"      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria")
country: "fi"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes)
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)
latitude: "60.209110"     # decimal latitude of workshop venue (use https://www.latlong.net/)
longitude: "24.964750"    # decimal longitude of the workshop venue (use https://www.latlong.net)
humandate: "March 19-20 2020"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "9:00 - 17:00"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2020-03-19      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2020-03-20        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Jarno Rantaharju","João M. da Silva","Juho Lehtonen"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Samantha Wittke"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["jarno.rantaharju@helsinki.fi"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:             # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

<h1> CANCELED </h1>

Due to the ongoing COVID-19 epidemic, we have decided to cancel the Software Carpentry event on March 19-20 2020. We apologize for any inconvenience caused. 

While we plan to run the event at a later date, we will decide on an exact time once the situation becomes more clear. 

In the meantime, all the materials for the course are available online and we encourage you to take the extra time to study them. If you do decide to self-study, the etherpad at <a href="https://pad.carpentries.org/adguAnQVNp-YGucJhiBH">https://pad.carpentries.org/adguAnQVNp-YGucJhiBH</a> will remain open for you to collaborate.

Jarno will be available for questions on the etherpad on Thursday March 19th and the preceding days.


{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
HEADER

Edit the values in the block above to be appropriate for your workshop.
If the value is not 'true', 'false', 'null', or a number, please use
double quotation marks around the value, unless specified otherwise.
And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}



{% comment %}
Check DC curriculum
{% endcomment %}

{% if site.carpentry == "dc" or site.carpentry == "dc" %}
{% unless site.curriculum == "dc-ecology" or site.curriculum == "dc-genomics" or site.curriculum == "dc-socsci" or site.curriculum == "dc-geospatial" %}
<div class="alert alert-warning">
It looks like you are setting up a website for a Data Carpentry curriculum but you haven't specified the curriculum type in the <code>_config.yml</code> file (current value in <code>_config.yml</code>: "<strong>{{ site.curriculum }}</strong>", possible values: <code>dc-ecology</code>, <code>dc-genomics</code>, <code>dc-socsci</code>, or <code>dc-geospatial</code>). After editing this file, you need to run <code>make serve</code> again to see the changes reflected.
</div>
{% endunless %}
{% endif %}


{% comment %}
EVENTBRITE

This block includes the Eventbrite registration widget if
'eventbrite' has been set in the header.  You can delete it if you
are not using Eventbrite, or leave it in, since it will not be
displayed if the 'eventbrite' field in the header is not set.
{% endcomment %}
{% if page.eventbrite %}
<iframe
  src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
  frameborder="0"
  width="100%"
  height="280px"
  scrolling="auto">
</iframe>
{% endif %}


<h2 id="general">General Information</h2>

{% comment %}
INTRODUCTION

Edit the general explanatory paragraph below if you want to change
the pitch.
{% endcomment %}
{% if site.carpentry == "swc" %}
{% include swc/intro.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}

{% comment %}
AUDIENCE

Explain who your audience is.  (In particular, tell readers if the
workshop is only open to people from a particular institution.
{% endcomment %}
{% if site.carpentry == "swc" %}
{% include swc/who.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}

{% comment %}
LOCATION

This block displays the address and links to maps showing directions
if the latitude and longitude of the workshop have been set.  You
can use https://itouchmap.com/latlong.html to find the lat/long of an
address.
{% endcomment %}
{% if page.latitude and page.longitude %}
<p id="where">
  <strong>Where:</strong>
  {{page.address}}.
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latitude}}&mlon={{page.longitude}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latitude}},{{page.longitude}}">Google Maps</a>.
</p>
{% endif %}

{% comment %}
DATE

This block displays the date and links to Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}.
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
REGISTRATION
{% endcomment %}

<strong>Registration:</strong> Registration is unfortunately closed. You can sign up to a waiting list at <a href="https://indico.neic.no/event/113/registrations"> https://indico.neic.no/event/113/registrations</a>. You can also check out other Software Carpentry and related events at <a href="https://carpentries.org/upcoming_workshops/"> the Software Carpentry site</a>. Also check out the similar 3-day workshops organized by <a href="https://coderefinery.org/workshops/">CodeRefinery</a>.

{% comment %}
SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
  <strong>Requirements:</strong> Participants must bring a laptop with a
  Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.). It should either be administered by the University of Helsinki or the participant should have administrative privileges on it. They should have a few specific software packages installed (listed <a href="#setup">below</a>).
</p>

{% comment%}
CODE OF CONDUCT
{% endcomment %}
<p id="code-of-conduct">
<strong>Code of Conduct:</strong>  Everyone who participates in Carpentries activities is required to conform to the <a href="https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html">Code of Conduct</a>. This document also outlines how to report an incident if needed.
</p>


{% comment %}
ACCESSIBILITY

Modify the block below if there are any barriers to accessibility or
special instructions.
{% endcomment %}
<p id="accessibility">
  <strong>Accessibility:</strong> We are committed to making this workshop
  accessible to everybody.
</p>
{% comment %}
  The workshop organizers have checked that:
<ul>
  <li>The room is wheelchair / scooter accessible.</li>
  <li>Accessible restrooms are available.</li>
</ul>
{% endcomment %}
<p>
  Materials will be provided in advance of the workshop and
  large-print handouts are available if needed by notifying the
  organizers in advance.  If we can help making learning easier for
  you (e.g. sign-language interpreters, lactation facilities) please
  get in touch (using contact details below) and we will
  attempt to provide them.
</p>

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
  {% for email in page.email %}
  {% if forloop.last and page.email.size > 1 %}
  or
  {% else %}
  {% unless forloop.first %}
  ,
  {% endunless %}
  {% endif %}
  <a href='mailto:{{email}}'>{{email}}</a>
  {% endfor %}
  {% else %}
  to-be-announced
  {% endif %}
  for more information.
</p>

<hr/>

{% comment %} 
SURVEYS - DO NOT EDIT SURVEY LINKS 
{% endcomment %}
<h2 id="surveys">Surveys</h2>
<p>Please be sure to complete these surveys before and after the workshop.</p>
<p><a href="{{ site.pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>

<hr/>


{% comment %}
SCHEDULE

Show the workshop's schedule.  Edit the items and times in the table
to match your plans.  You may also want to change 'Day 1' and 'Day
2' to be actual dates or days of the week.
{% endcomment %}
<h2 id="schedule">Schedule</h2>

<div class="row">
  <div class="col-md-6">
    <h3>Thursday</h3>
    <table class="table table-striped">
      <tr> <td>Before</td> <td><a href="{{ site.pre_survey }}{{ site.github.project_title }}">Pre-workshop survey</a> </td> </tr>
      <tr> <td>09:00</td>  <td>Automating Tasks with the Unix Shell</td> </tr>
      <tr> <td>10:30</td>  <td>Morning break</td> </tr>
      <tr> <td>11:00</td>  <td>Automating Tasks with the Unix Shell (Continued)</td> </tr>
      <tr> <td>12:00</td>  <td>Lunch break</td> </tr>
      <tr> <td>13:00</td>  <td>Building Programs with Python</td> </tr>
      <tr> <td>14:30</td>  <td>Afternoon break</td> </tr>
      <tr> <td>15:00</td>  <td>Building Programs with Python (Continued)</td> </tr>
      <tr> <td>16:00</td>  <td>Wrap-up</td> </tr>
      <tr> <td>16:30</td>  <td>END</td> </tr>
    </table>
  </div>
  <div class="col-md-6">
    <h3>Friday</h3>
    <table class="table table-striped">
      <tr> <td>09:00</td>  <td>Version Control with Git</td> </tr>
      <tr> <td>10:30</td>  <td>Morning break</td> </tr>
      <tr> <td>11:00</td>  <td>Version Control with Git (Continued)</td> </tr>
      <tr> <td>12:00</td>  <td>Lunch break</td> </tr>
      <tr> <td>13:00</td>  <td>Building Programs with Python (Continued)</td> </tr>
      <tr> <td>14:30</td>  <td>Afternoon break</td> </tr>
      <tr> <td>15:00</td>  <td>Building Programs with Python (Continued)</td> </tr>
      <tr> <td>16:00</td>  <td>Wrap-up</td> </tr>
      <tr> <td>16:30</td>  <td><a href="{{ site.post_survey }}{{ site.github.project_title }}" target="_blank">Post-workshop Survey</a></td> </tr>
      <tr> <td>16:40</td>  <td>END</td> </tr>
    </table>
  </div>
</div>


{% comment %}
Collaborative Notes

If you want to use an Etherpad, go to

http://pad.carpentries.org/YYYY-MM-DD-site

where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.
{% endcomment %}
{% if page.collaborative_notes %}
<p id="collaborative_notes">
  We will use this <a href="{{page.collaborative_notes}}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
{% endif %}

<hr/>

{% comment %}
SYLLABUS

Show what topics will be covered.

1. If your workshop is R rather than Python, remove the comment
around that section and put a comment around the Python section.
2. Some workshops will delete SQL.
3. Please make sure the list of topics is synchronized with what you
intend to teach.
4. You may need to move the div's with class="col-md-6" around inside
the div's with class="row" to balance the multi-column layout.

This is one of the places where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}
<h2 id="syllabus">Syllabus</h2>

<div class="row">
  <div class="col-md-6">
    <h3 id="syllabus-shell">The Unix Shell</h3>
    <ul>
      <li>Files and Directories</li>
      <li>History and Tab Completion</li>
      <li>Pipes and Redirection</li>
      <li>Looping Over Files</li>
      <li>Creating and Running Shell Scripts</li>
      <li>Finding Things</li>
      <li><a href="{{site.swc_pages}}/shell-novice/reference">Reference...</a></li>
    </ul>
  </div>
  <div class="col-md-6">
    <h3 id="syllabus-python">Programming in Python</h3>
    <ul>
      <li>Using Libraries</li>
      <li>Working with Arrays</li>
      <li>Reading and Plotting Data</li>
      <li>Creating and Using Functions</li>
      <li>Loops and Conditionals</li>
      <li>Defensive Programming</li>
      <li>Using Python from the Command Line</li>
      <li><a href="{{site.swc_pages}}/python-novice-inflammation/reference">Reference...</a></li>
    </ul>
  </div>
  <!--
  <div class="col-md-6">
    <h3 id="syllabus-r">Programming in R</h3>
    <ul>
      <li>Working with Vectors and Data Frames</li>
      <li>Reading and Plotting Data</li>
      <li>Creating and Using Functions</li>
      <li>Loops and Conditionals</li>
      <li>Using R from the Command Line</li>
      <li><a href="{{site.swc_pages}}/r-novice-inflammation/reference">Reference...</a></li>
    </ul>
  </div>
  -->
  <!--
  <div class="col-md-6">
    <h3 id="syllabus-matlab">Programming in MATLAB</h3>
    <ul>
      <li>Working with Arrays</li>
      <li>Reading and Plotting Data</li>
      <li>Creating and Using Functions</li>
      <li>Loops and Conditionals</li>
      <li>Defensive Programming</li>
      <li><a href="{{site.swc_pages}}/matlab-novice-inflammation/reference">Reference...</a></li>
     </ul>
   </div>
   -->
</div>

<div class="row">
  <div class="col-md-6">
    <h3 id="syllabus-git">Version Control with Git</h3>
    <ul>
      <li>Creating a Repository</li>
      <li>Recording Changes to Files: <code>add</code>, <code>commit</code>, ...</li>
      <li>Viewing Changes: <code>status</code>, <code>diff</code>, ...</li>
      <li>Ignoring Files</li>
      <li>Working on the Web: <code>clone</code>, <code>pull</code>, <code>push</code>, ...</li>
      <li>Resolving Conflicts</li>
      <li>Open Licenses</li>
      <li>Where to Host Work, and Why</li>
      <li><a href="{{site.swc_pages}}/git-novice/reference">Reference...</a></li>
    </ul>
  </div>
  <!--
  <div class="col-md-6">
    <h3 id="syllabus-sql">Managing Data with SQL</h3>
    <ul>
      <li>Reading and Sorting Data</li>
      <li>Filtering with <code>where</code></li>
      <li>Calculating New Values on the Fly</li>
      <li>Handling Missing Values</li>
      <li>Combining Values Using Aggregation</li>
      <li>Combining Information From Multiple Tables Using <code>join</code></li>
      <li>Creating, Modifying, and Deleting Data</li>
      <li>Programming with Databases</li>
      <li><a href="{{site.swc_pages}}/sql-novice-survey/reference">Reference...</a></li>
    </ul>
  </div>
  -->
    <!--
  <div class="col-md-6">
    <h3 id="syllabus-r">Open Refine</h3>
    <ul>
      <li>Introduction to OpenRefine</li>
      <li>Importing Data</li>
      <li>Basic Functions</li>
      <li>Advanced Functions</li>
      <li><a href="{{site.lc_pages}}library-openrefine/reference">Reference...</a></li>
    </ul>
  </div>-->
</div>

<hr/>

{% comment %}
SETUP

Delete irrelevant sections from the setup instructions.  Each
section is inside a 'div' without any classes to make the beginning
and end easier to find.

This is the other place where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.
{% endcomment %}

<h2 id="setup">Setup</h2>

<p>
  To participate in a
  {% if site.carpentry == "swc" %}
  Software Carpentry
  {% elsif site.carpentry == "dc" %}
  Data Carpentry
  {% elsif site.carpentry == "lc" %}
  Library Carpentry
  {% endif %}
  workshop,
  you will need access to the software described below.
  In addition, you will need an up-to-date web browser.
</p>
<p>
  We maintain a list of common issues that occur during installation as a reference for instructors
  that may be useful on the
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Configuration Problems and Solutions wiki page</a>.
</p>

<div id="HY">
  <h3>Helsinki University Administrated Laptops</h3>
  <p>
  If you have a laptop administered by the University of Helsinki, you can use the Software Center to install the required applications.
  </p>

  <div>
    <ul class="nav nav-tabs nav-justified" role="tablist">
      <li role="presentation" class="active"><a data-os="windows" href="#hy-windows" aria-controls="Windows"   role="tab" data-toggle="tab">Windows</a></li>
      <li role="presentation"><a data-os="macos" href="#hy-macos" aria-controls="MacOS" role="tab"   data-toggle="tab">MacOS</a></li>
      <li role="presentation"><a data-os="linux" href="#hy-linux" aria-controls="Linux" role="tab"   data-toggle="tab">Linux</a></li>
    </ul>
    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="hy-windows">
      <p>
        On Windows laptops, you will need to install two applications:
        <ol>
          <li> Git for Windows and </li>
          <li> Anaconda. </li>
        </ol>
        Follow the instructions below when the installation wizard asks provides you with options.
      </p>
      </article>
    </div>
    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="hy-macos">
      <p>
        On MacOS, you can install Git through the App store.
        <b> Please contact the Helpdesk (helpdesk@helsinki.fi) to install Anaconda. </b>
      </p>
      </article>
    </div>
    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="hy-linux">
      <p>
        Cubbli Linux comes with all required software pre-installed.
      </p>
      </article>
    </div>
  </div>
</div>


<div id="shell"> {% comment %} Start of 'shell' section. {% endcomment %}
  <h3>The Bash Shell</h3>
  <p>
    Bash is a commonly-used shell that gives you the power to do simple
    tasks more quickly.
  </p>

  <div>
    <ul class="nav nav-tabs nav-justified" role="tablist">
      <li role="presentation" class="active"><a data-os="windows" href="#shell-windows" aria-controls="Windows" role="tab" data-toggle="tab">Windows</a></li>
      <li role="presentation"><a data-os="macos" href="#shell-macos" aria-controls="MacOS" role="tab" data-toggle="tab">MacOS</a></li>
      <li role="presentation"><a data-os="linux" href="#shell-linux" aria-controls="Linux" role="tab" data-toggle="tab">Linux</a></li>
    </ul>

    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="shell-windows">
        <a href="https://www.youtube.com/watch?v=339AEqk9c-8">Video Tutorial</a>
        <ol>
          <li>Download the Git for Windows <a href="https://git-for-windows.github.io/">installer</a>.</li>
          <li>Run the installer and follow the steps below:
            <ol>
              {% comment %} Git 2.23.0 Setup {% endcomment %}
              <li>
                Click on "Next" four times (two times if you've previously
                installed Git).  You don't need to change anything
                in the Information, location, components, and start menu screens.
              </li>
              <li>
                <strong>
                  From the dropdown menu select "Use the nano editor by default" and click on "Next".
                </strong>
              </li>
              {% comment %} Adjusting your PATH environment {% endcomment %}
              <li>
                Ensure that "Git from the command line and also from 3rd-party software" is selected and
                click on "Next". (If you don't do this Git Bash will not work properly, requiring you to
                remove the Git Bash installation, re-run the installer and to select the "Git from the
                command line and also from 3rd-party software" option.)
              </li>
              {% comment %} Choosing the SSH executable {% endcomment %}
              {% comment %} Choosing HTTPS transport backend {% endcomment %}
              <li>
		Ensure that "Use the native Windows Secure Channel library" is selected and click on "Next".
	      </li>
              {% comment %} This should mean that people stuck behind corporate firewalls that do MITM attacks
                                 with their own root CA are still able to access remote git repos. {% endcomment %}
              {% comment %} Configuring the line ending conversions {% endcomment %}
              <li>
                Ensure that "Checkout Windows-style, commit Unix-style line endings" is selected and click on "Next".
              </li>
              {% comment %} Configuring the terminal emulator to use with Git Bash {% endcomment %}
              <li>
                <strong>
                  Ensure that "Use Windows' default console window" is selected and click on "Next".
                </strong>
              </li>
              {% comment %} Configuring extra options {% endcomment %}
              <li>
		Ensure that "Enable file system caching" and "Enable Git Credential Manager" are selected
		and click on "Next".
              </li>
              {% comment %} Configuring experimental options {% endcomment %}
              <li>Click on "Install".</li>
              {% comment %} Installing {% endcomment %}
              {% comment %} Completing the Git Setup Wizard {% endcomment %}
              <li>Click on "Finish".</li>
            </ol>
          </li>
          <li>
            If your "HOME" environment variable is not set (or you don't know what this is):
            <ol>
              <li>Open command prompt (Open Start Menu then type <code>cmd</code> and press [Enter])</li>
              <li>
                Type the following line into the command prompt window exactly as shown:
                <p><code>setx HOME "%USERPROFILE%"</code></p>
              </li>
              <li>Press [Enter], you should see <code>SUCCESS: Specified value was saved.</code></li>
              <li>Quit command prompt by typing <code>exit</code> then pressing [Enter]</li>
            </ol>
          </li>
          
          
          
          
        </ol>
        <p>This will provide you with both Git and Bash in the Git Bash program.</p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="shell-macos">
        <p>
          The default shell in all versions of macOS is Bash, so no
          need to install anything.  You access Bash from the Terminal
          (found in
          <code>/Applications/Utilities</code>).
          See the Git installation <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">video tutorial</a>
          for an example on how to open the Terminal.
          You may want to keep
          Terminal in your dock for this workshop.
        </p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="shell-linux">
        <p>
          The default shell is usually Bash, but if your
          machine is set up differently you can run it by opening a
          terminal and typing <code>bash</code>.  There is no need to
          install anything.
        </p>
      </article>
    </div>
  </div>
</div> {% comment %} End of 'shell' section. {% endcomment %}

<div id="git"> {% comment %} Start of 'Git' section. GitHub browser compatibility
  is given at https://help.github.com/articles/supported-browsers/{% endcomment %}
  <h3>Git</h3>
  <p>
    Git is a version control system that lets you track who made changes
    to what when and has options for easily updating a shared or public
    version of your code
    on <a href="https://github.com/">github.com</a>. You will need a
    <a href="https://help.github.com/articles/supported-browsers/">supported
    web browser</a>.
  </p>
  <p>
    You will need an account at <a href="https://github.com/">github.com</a>
    for parts of the Git lesson. Basic GitHub accounts are free. We encourage
    you to create a GitHub account if you don't have one already.
    Please consider what personal information you'd like to reveal. For
    example, you may want to review these
    <a href="https://help.github.com/articles/keeping-your-email-address-private/">instructions
      for keeping your email address private</a> provided at GitHub.
  </p>

  <div>
    <ul class="nav nav-tabs nav-justified" role="tablist">
      <li role="presentation" class="active"><a data-os="windows" href="#git-windows" aria-controls="Windows" role="tab" data-toggle="tab">Windows</a></li>
      <li role="presentation"><a data-os="macos" href="#git-macos" aria-controls="MacOS" role="tab" data-toggle="tab">MacOS</a></li>
      <li role="presentation"><a data-os="linux" href="#git-linux" aria-controls="Linux" role="tab" data-toggle="tab">Linux</a></li>
    </ul>

    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="git-windows">
        <p>
          Git should be installed on your computer as part of your Bash
          install (described above).
        </p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="git-macos">
        <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">Video Tutorial</a>
        <p>
          <strong>For OS X 10.9 and higher</strong>, install Git for Mac
          by downloading and running the most recent "mavericks" installer from
          <a href="http://sourceforge.net/projects/git-osx-installer/files/">this list</a>.
          Because this installer is not signed by the developer, you may have to
          right click (control click) on the .pkg file, click Open, and click
          Open on the pop up window.
          After installing Git, there will not be anything in your <code>/Applications</code> folder,
          as Git is a command line program.
          <strong>For older versions of OS X (10.5-10.8)</strong> use the
          most recent available installer labelled "snow-leopard"
          <a href="http://sourceforge.net/projects/git-osx-installer/files/">available here</a>.
        </p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="git-linux">
        <p>
          If Git is not already available on your machine you can try to
          install it via your distro's package manager. For Debian/Ubuntu run
          <code>sudo apt-get install git</code> and for Fedora run
          <code>sudo dnf install git</code>.
        </p>
      </article>
    </div>
  </div>
</div> {% comment %} End of 'Git' section. {% endcomment %}

<div id="editor"> {% comment %} Start of 'editor' section. {% endcomment %}
  <h3>Text Editor</h3>

  <p>
    When you're writing code, it's nice to have a text editor that is
    optimized for writing code, with features like automatic
    color-coding of key words. The default text editor on macOS and
    Linux is usually set to Vim, which is not famous for being
    intuitive. If you accidentally find yourself stuck in it, hit
    the <kbd>Esc</kbd> key, followed by <kbd>:</kbd>+<kbd>Q</kbd>+<kbd>!</kbd>
    (colon, lower-case 'q', exclamation mark), then hitting <kbd>Return</kbd> to
    return to the shell.
  </p>

  <div>
    <ul class="nav nav-tabs nav-justified" role="tablist">
      <li role="presentation" class="active"><a data-os="windows" href="#editor-windows" aria-controls="Windows" role="tab" data-toggle="tab">Windows</a></li>
      <li role="presentation"><a data-os="macos" href="#editor-macos" aria-controls="MacOS" role="tab" data-toggle="tab">MacOS</a></li>
      <li role="presentation"><a data-os="linux" href="#editor-linux" aria-controls="Linux" role="tab" data-toggle="tab">Linux</a></li>
    </ul>

    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="editor-windows">
        <p>
          nano is a basic editor and the default that instructors use in the workshop.
          It is installed along with Git.
        </p>
        <p>
          Others editors that you can use are
          <a href="https://notepad-plus-plus.org/">Notepad++</a> or
          <a href="https://www.sublimetext.com/">Sublime Text</a>.
          <strong>Be aware that you must
            add its installation directory to your system path.</strong>
          Please ask your instructor to help you do this.
        </p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="editor-macos">
        <p>
          nano is a basic editor and the default that instructors use in the workshop.
          See the Git installation <a href="https://www.youtube.com/watch?v=9LQhwETCdwY ">video tutorial</a>
          for an example on how to open nano.
          It should be pre-installed.
        </p>
        <p>
          Others editors that you can use are
          <a href="https://www.barebones.com/products/bbedit/">BBEdit</a> or
          <a href="https://www.sublimetext.com/">Sublime Text</a>.
        </p>
      </article>
      <article role="tabpanel" class="tab-pane active" id="editor-linux">
        <p>
          nano is a basic editor and the default that instructors use in the workshop.
          It should be pre-installed.
        </p>
        <p>
          Others editors that you can use are
          <a href="https://wiki.gnome.org/Apps/Gedit">Gedit</a>,
          <a href="https://kate-editor.org/">Kate</a> or
          <a href="https://www.sublimetext.com/">Sublime Text</a>.
        </p>
      </article>
    </div>
  </div>
</div> {% comment %} End of 'editor' section. {% endcomment %}

<div id="python"> {% comment %} Start of 'Python' section. Remove the third paragraph if
  the workshop will teach Python using something other than
  the Jupyter notebook.
  Details at https://jupyter-notebook.readthedocs.io/en/stable/notebook.html#browser-compatibility {% endcomment %}
  <h3>Python</h3>

  <p>
    <a href="https://python.org">Python</a> is a popular language for
    research computing, and great for general-purpose programming as
    well.  Installing all of its research packages individually can be
    a bit difficult, so we recommend
    <a href="https://www.anaconda.com/distribution/">Anaconda</a>,
    an all-in-one installer.
  </p>

  <p>
    Regardless of how you choose to install it,
    <strong>please make sure you install Python version 3.x</strong>
    (e.g., 3.6 is fine).
  </p>

  <p>
    We will teach Python using the <a href="https://jupyter.org/">Jupyter notebook</a>,
    a programming environment that runs in a web browser. For this to work you will need a reasonably
    up-to-date browser. The current versions of the Chrome, Safari and
    Firefox browsers are all
    <a href="https://jupyter-notebook.readthedocs.io/en/stable/notebook.html#browser-compatibility">supported</a>
    (some older browsers, including Internet Explorer version 9
    and below, are not).
  </p>

  <div>
    <ul class="nav nav-tabs nav-justified" role="tablist">
      <li role="presentation" class="active"><a data-os="windows" href="#python-windows" aria-controls="Windows" role="tab" data-toggle="tab">Windows</a></li>
      <li role="presentation"><a data-os="macos" href="#python-macos" aria-controls="MacOS" role="tab" data-toggle="tab">MacOS</a></li>
      <li role="presentation"><a data-os="linux" href="#python-linux" aria-controls="Linux" role="tab" data-toggle="tab">Linux</a></li>
    </ul>

    <div class="tab-content">
      <article role="tabpanel" class="tab-pane active" id="python-windows">
        <a href="https://www.youtube.com/watch?v=xxQ0mzZ8UvA">Video Tutorial</a>
        <ol>
          <li>Open <a href="https://www.anaconda.com/download/#windows">https://www.anaconda.com/download/#windows</a> with your web browser.</li>
          <li>Download the Python 3 installer for Windows.</li>
          <li>Install Python 3 using all of the defaults for installation <em>except</em> make sure to check <strong>Add Anaconda to my PATH environment variable</strong>.</li>
        </ol>
      </article>
      <article role="tabpanel" class="tab-pane active" id="python-macos">
        <a href="https://www.youtube.com/watch?v=TcSAln46u9U">Video Tutorial</a>
        <ol>
          <li>Open <a href="https://www.anaconda.com/download/#macos">https://www.anaconda.com/download/#macos</a> with your web browser.</li>
          <li>Download the Python 3 installer for OS X.</li>
          <li>Install Python 3 using all of the defaults for installation.</li>
        </ol>
      </article>
      <article role="tabpanel" class="tab-pane active" id="python-linux">
        <ol>
          <li>Open <a href="https://www.anaconda.com/download/#linux">https://www.anaconda.com/download/#linux</a> with your web browser.</li>
          <li>Download the Python 3 installer for Linux.<br>
            (The installation requires using the shell. If you aren't
            comfortable doing the installation yourself
            stop here and request help at the workshop.)
          </li>
          <li>
            Open a terminal window.
          </li>
          <li>
            Type <pre>bash Anaconda3-</pre> and then press
            <kbd>Tab</kbd>. The name of the file you just downloaded should
            appear. If it does not, navigate to the folder where you
            downloaded the file, for example with:
            <pre>cd Downloads</pre>
            Then, try again.
          </li>
          <li>
            Press <kbd>Return</kbd>. You will follow the text-only prompts. To move through
            the text, press <kbd>Spacebar</kbd>. Type <code>yes</code> and
            press enter to approve the license. Press enter to approve the
            default location for the files. Type <code>yes</code> and
            press enter to prepend Anaconda to your <code>PATH</code>
            (this makes the Anaconda distribution the default Python).
          </li>
          <li>
            Close the terminal window.
          </li>
        </ol>
      </article>
    </div>
  </div>
  {% comment %}
  <p>
    Once you are done installing the software listed above,
    please go to <a href="setup/index.html">this page</a>,
    which has instructions on how to test that everything was installed correctly.
  </p>
  {% endcomment %}
</div> {% comment %} End of 'Python' section. {% endcomment %}


