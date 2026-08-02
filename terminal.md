---
layout: terminal
title: Home
---
<script>
    var greetings = `
Welcome to
       __                __        
  ____/ /___ ____  ___  / /_  _____
 / __  / __ \`/ _ \\/ _ \\/ __ \\/ ___/
/ /_/ / /_/ /  __/  __/ /_/ (__  ) 
\\__,_/\\__, /\\___/\\___/_.___/____/  
     /____/                       
     
Type 'help' for a list of available commands...`;

    var helpText = `TOPIC
    DgeebsShell Help System

SHORT DESCRIPTION
    Displays help about DgeebsShell cmds and concepts.

LONG DESCRIPTION
    DgeebsShell Help describes DgeebsSheel cmds,
    functions, modules, and explains content available.

EXAMPLES
    Get-Info all        : Lists all avaiable info about dgeebs
    Get-Info about      : Lists about info about dgeebs
    Get-Info skills     : Lists skills info about dgeebs
    Get-Info experience : Lists experience info about dgeebs
    Get-Info projects   : Lists current and past projects by dgeebs
    Get-Info contact    : Lists contact info of dgeebs
`;
    var about = `
ABOUT

Hey, I'm Daniel! 👋
I love to design, build, grow, and create.
I think great communication, collaboration, sharing and storyteling are paramount to the success of any endeavor.
I feel like we could make something great together!
`;
    var experience = `
EXPERIENCE

    AVERTIUM - 
    - 

    TERRA VERDE - 
    - 
`;
    var skills = `
SKILLS

I am a...
    - Full stack developer, versed in nodejs, react, python, html, sql, and css
    - Sr security architect, heavy on the architect. I have designe, implemented, implemented and maintained applications, integrations, and solutions to enable a managed security services provider’s 24/7/365 security operations center to centrally collect, analyze, and triage security alerts for over 150+ MSSP customers.
    - Administrator, I have in depth experience using and administering ticketing platforms such as OTRS, ServiceNow, and Connectwise
    - Security Professional, for a period of time I worked as a penetration tester and earned my OSCP from offensive security
    - Cloud engineer, AWS and Azure
`;

    $('body').terminal({
        hello: function(what) {
            this.echo('Hello, ' + what +
                    '. Wellcome to this terminal.');
        },
        help: function(){
            this.echo(helpText);
        },
        'Get-Info': function(section){
            switch(section){
                case("about"):
                    this.echo(about);
                    break;
                case("skills"):
                    this.echo(skills);
                    break;
                case("experience"):
                    this.echo(experience);
                    break;
                default:
                    this.echo("dump everything");
            }
        }
    }, {
        greetings: greetings
    });
</script>