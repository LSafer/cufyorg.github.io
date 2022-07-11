---
layout: default 
permalink: / 
section: Home 
links:
    Android: https://cufyx.org
    GitHub: https://github.com/cufyorg
    Patreon: https://patreon.com/cufy
    YouTube: https://youtube.com/channel/UCQrEzyMcfnvfNG6irFRBePg
    Discord: https://discord.gg/ASAGGy7
    Gitter: https://gitter.im/cufyorg/community
    Twitter: https://twitter.com/cufyorg
---

Cufy is an non-profit open-source international organization focused on gathering variant
kinds of programmers from beginners to professionals so members learn from another.
Because Cufy is a nonprofit organization, the main target of Cufy members is friendship,
experience and popularity. This website lists the main projects of Cufy.

<hr>
<br>

## <a href="https://jamplate.org">Jamplate</a>

Jamplate is a C-Style pre-processor. Although it is a C-Style, this does not mean it is
following the C standard. This pre-processor has almost the same expected behaviour as a
standard C pre-processors with some features added and some missing.

[![Jamplate][repo_jamplate]][github_jamplate]

<pre class="prettyprint language-jamplate">
	#for $output ['firstfile', 'secondfile', 'thirdfile', 'forthfile']
	#console __OUTPUT__ '/' $output '.txt'
	#include __PROJECT__ '/myheader.jh'

	#message 'generating "' $output '.txt" ...' "\n"

	#if $output == 'firstfile'
	#message 'its the first file' "\n"
	#elif $output == 'secondfile'
	#message 'its the second file' "\n"
	#else
	#message 'its not the first nor the second file' "\n"
	#endif

	#ifndef __JAMPLATE__
	#error 'You are not using the jamplate processor!' "\n"
	#endif

	#declare $line __LINE__ + 1
	This file was auto generated from the file #{__FILE__}# on #{__DATE__}#
	at #{__TIME__}# using "Jamplate Processor #{__JAMPLATE__}#" and this 
	paragraph starts at line #{$line}#.
	#endfor
</pre>

<br>

## <a href="https://github.com/cufyorg/mangaka">Mangaka</a>

A `mongodb`, `mongoose` equivilant driver for `kotlin`.

[![Mangaka][repo_mangaka]][github_mangaka]

<br>

## <a href="https://github.com/cufyorg/kaguya">Kaguya</a>

A `kotlin`-friendly wrapper for `graphql-java` with `ktor` integration

[![Mangaka][repo_kaguya]][github_kaguya]

<br>


## <a href="https://github.com/cufyorg/openperm-kt">Openperm</a>

A `kotlin` permission/authorization calculator. 

[![Mangaka][repo_openperm-kt]][github_openperm-kt]

<br>

## <a href="https://github.com/cufyorg/http">Http</a>

A java builder-style customizable http client that can integrate with other Http client
libraries to combine speed and customizability. Writing then sending an HTTP request might
be done in a few lines and with one statement, including: setting the headers, writing the
body writing the query, etc. This library also has a supporting library for android
providing help for synchronization and storing the Context.

[![Http][repo_http]][github_http]

<br>

[github_mangaka]: https://github.com/cufyorg/mangaka
[repo_mangaka]: https://github-readme-stats.vercel.app/api/pin?username=cufyorg&repo=mangaka&show_owner=1&theme=dracula&border_color=333333&bg_color=333333

[github_kaguya]: https://github.com/cufyorg/kaguya
[repo_kaguya]: https://github-readme-stats.vercel.app/api/pin?username=cufyorg&repo=kaguya&show_owner=1&theme=dracula&border_color=333333&bg_color=333333

[github_openperm-kt]: https://github.com/cufyorg/openperm-kt
[repo_openperm-kt]: https://github-readme-stats.vercel.app/api/pin?username=cufyorg&repo=openperm-kt&show_owner=1&theme=dracula&border_color=333333&bg_color=333333

[github_jamplate]: https://github.com/jamplate/processor
[repo_jamplate]: https://github-readme-stats.vercel.app/api/pin?username=jamplate&repo=processor&show_owner=1&theme=dracula&border_color=333333&bg_color=333333

[github_http]: https://github.com/cufyorg/http
[repo_http]: https://github-readme-stats.vercel.app/api/pin?username=cufyorg&repo=http&show_owner=1&theme=dracula&border_color=333333&bg_color=333333

<style>
    a img {
        background: #333333;
        margin: 50px 0 0 20px;
        /*background: radial-gradient(rgb(80, 27, 127), rgb(90, 27, 127), rgb(95, 27, 127), rgb(90, 27, 127), rgb(80, 27, 127), rgb(90, 27, 127));*/
        border-radius: 5pt;
        box-shadow: 0 0 5px 1px gray;
        padding: 20px;
        color: whitesmoke;
    }

    @media (max-width: 720px) {
        a img {
            display: none;
        }
    }
</style>
