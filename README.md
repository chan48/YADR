     _     _           _
    | |   | |         | |
    | |___| |_____  __| | ____
    |_____  (____ |/ _  |/ ___)
     _____| / ___ ( (_| | |
    (_______\_____|\____|_|

    # Yet Another Dotfile Repo v1.0
    # Now with Prezto!

    git clone https://github.com/skwp/dotfiles ~/.yadr
    cd ~/.yadr && rake install

This is a collection of best of breed tools from across the web,
from scouring other people's dotfile repos, blogs, and projects.


>주의: 겉보기에 좋아보여 무작정 설치하고 난 뒤, vim 키맵이 변경되서 빡치지 않게 사전에 잘 읽어보셈  


## YADR은 또 뭔데?

**YADR is an opinionated dotfile repo that will make your heart sing**

  * 맥은 겁나 좋은 운영체제 잖아? MacVim 역시 최고의 편집기! Zsh도.. 최고의 셸? 글구,, Pry .. Solarized 역시 최고의 컬러 스키마지. 
  * 애플 스타일 철학을 적용시켰다. 걍 모든게 제대로 동작하고 보기 끝내줘. 옵션이 많다고 겁먹지 마셈.
  * 자주 쓰는 모든 명령어는 두세자로 된 줄임말이 지원되니 손가락을 움직이는게 덜할거야. 
  * 몇가지 빡치는 키맵을 피하고 vim에서 윈도우 관리도 쉽다. 
  * 플러그인 아키텍트가 사용하기 쉽게 되어 있고 설정파일도 건드릴게 없어. (뻥이야;;)
  * 걍 하나 골라서 어디에나 적용하셈. vim 이 짱먹는 세상!
  * 겁나 이쁘고 읽기 편하고 쌈빡한 vimrc를 제공한다네.. **
  * 키 오버라이딩이나 해킹짓거리를 안해. 걍 모든 설정은 .vim/plugin/settings 아래에 있어. 
  * Janus보다 vim 플러그인 리스트가 많은데다 Ruby/Rails/Git 개발환경으로 잘 맞아 떨어지지. 
  * Solarized 색상 스키마에 최적화 되어 있어서 일단 보는 것은 끝내준다. 눈이 호강할거야. 
  * 모든 플러그인은 Solarized와 테스트 했고 특정 색상을 쓴 곳은 눈이 아프지 않도록 신경쓰이는 곳에 적용했다.
  * 설정파일은 관리할 필요없어. YADR은 겁나 간단한 ruby 스크립트 파일로 git submodule을 관리하는데 쓸일뿐이야.
  * 플러그인 파일과 동떨어져 vimrc 파일 내용이 일단 깔끔해. 
  * 키맵파일과 기타 설정은 .vim/plugins/settings 아래에서 관리해야해 
  * vim 플러그인 그 이상의 집합이라고나 할까.. - 있어보이는 명령어 별명과 기타 osx,irb/pry 트윅들로 딴짓거리하는데 최고의 환경을 제공한다네~!

## 스크린샷
![screenshot](http://i.imgur.com/3C1Ze.png)

# 설치과정

`rake`와 `yadr`명령어로 자동 설치되니 걍 생각하지 말고 Copy & Paste 하면되:

```bash
git clone https://github.com/skwp/dotfiles ~/.yadr
cd ~/.yadr && rake install
```

**주의하지마:** YADR은 하위 컴포넌트를 자동으로 설치하므로 각 항목마다 동의를 받고 싶으면 다음과 같이 실행한다: `ASK=true rake install`

### 업데이트 하기

겁나 쉽게 된다.

```bash
cd ~/.yadr
git pull origin master
rake update
```

# 근까.. 뭐가 들어있는데? 글구 어떻게 고치냐?

귀찮지만 YADR을 좀 사용하고 싶다면 계속 읽어.

### Public service announcement: 손가락에 테러를 가하지 말자~!

[Remap caps-lock to escape with PCKeyboardHack](http://pqrs.org/macosx/keyremap4macbook/pckeyboardhack.html)

ESC 키는 vim 에서 겁나 중요하고 많이 쓰이는 키인데 옛날에 나온 키보드는 컨트롤키(CTRL)가 캡스락(CapsLock) 자리에 있어서 그 자리를 ESC에다 배정하면 좋을수도 있잖아?
자꾸 구석탱이에 있는 작은 걸 치다보면 겁나게 작업이 느려질 수 있으고 손도 망가지고,,,  (-__- ;;; 된장)

### [Homebrew](http://mxcl.github.com/homebrew/)

Homebrew는 OSX 배포본과 같이 있어야 하는데 애플 애들이 빠트린거야. 자동으로 설치할 것임. 

글구, 몇가지 필요한 것들을 설치할 건데,, ack, ctags, git,hub 등등이지. macvim은 brew를 통해 설치하든가 아니면 걔네들 웹사이트에서 받아서 넣어도 되.

```bash
brew install ack ctags git hub macvim tmux reattach-to-user-namespace
```

### Github 소식: [ghi gem](https://github.com/stephencelis/ghi)

`ghi` 명령어도 설치된다. `ghi list` 명령을 때려보면 콘솔로 폼나게 이슈를 관리할 수 있을거야.

### Ruby 디버거

이건 옵션이라 포함되어 있지않다. vim에서 있어보이는 IDE 스타일의 디버깅을 할때 쓰이는데 쓸려면 다음과 같이 플러그인을 설치하셈:

```bash
gem install ruby-debug-ide
```

### ZSH

bash를 줄곧 써왔는데 요즘은 ZSH을 쓰고있다.  기본 셸로 대체해서 쓰는데,  이거 좀 죽여주거든. 특히 globbing이랑 자동 완성 기능은 짱먹고 있음. 
bash에서 zsh로 마이그레이트하는데 별 문제없고 zshrc 에서 몇몇 기능을 보강해주는데 히스토리를 거꾸로 검색하는 Ctrl-R 같은 거 말야..

매일 매일 사용하는 명령어는 대부분 몇글자로 처리하지. 마구 마구 고쳐도 되:

    ae # alias edit
    ar # alias reload

### [Prezto](https://github.com/sorin-ionescu/prezto)

Zsh를 제대로 쓰려고 **[Prezto](http://github.com/sorin-ionescu/prezto)**를 서브모듈로 이미 포함하고 있음.

### 각자 스타일의 테마를 ZSH에 추가하기

스타일 대로 쓰고 싶다면 ~/.zsh.prompts 에 넣어 두면 됨. 자동으로 처리될 것임. 근데, 이름짓는 규정대로 `prompt_[name]_setup` 처럼 했는지 확인해야함. 

```
touch ~/.zsh.prompts/prompt_mytheme_setup
```

~/.yadr/zsh/prezto-themes/prompt_skwp_setup 에서 예제를 보고 어떻게 프롬프트를 쓰는지 확인해보셈. 
[Prezto](https://github.com/sorin-ionescu/prezto) 프로젝트에 더 자세한 사항이 있음.

### ZSH 손좀 보기 & 테마 선택하기 

zsh 환경을 좀 손좀 보려면  ~/.zsh.after/ 하고 ~/.zsh.before/ 디렉토리 두개의 yadr 훅을 손봐야 함: 그 폴더에서 ~/.yadr/zsh/* 에 있는 다른 zsh 설정파일을 읽기 전이나 후에 적용할 것들을 넣어 두면 되는거지.

예를들어, 테마를 오버랑이딩 하려면 이것 처럼 하든가:
```
echo "prompt skwp" > ~/.zsh.after/prompt.zsh
```

다음번에 셸이 뜰때 읽혀지고 skwp(?) 프롬프트가 적용될거야. `prompt -l` 하면 사용가능한 프롬프트가 뜰 것임.

### 이미 적용되어 있는 ZSH 커스토마이즈 설정들

 * Vim 모드!!!
 * Bash 스타일의 ctrl-R로 히스토리를 거꾸로 검색
 * 마지막 명령어의 출력을 끼워 넣기: Ctrl-x,Ctrl-l
 * Fuzzy 매칭 - 폴더 이름을 잘못 쓰거나 했더라도 탭을 누르면  이름을 고쳐서 완성해줘~!
 * [fasd](https://github.com/clvv/fasd) 통합되어 있음 - 최근 사용된 폴더를  `z`키와 탭을 눌러 자동완성할 수있음.
 * 입력하는 것에 따라 문법 강조
 * 글구, 더 많다!

### [Pry](http://pry.github.com/) 
Pry offers a much better out of the box IRB experience with colors, tab completion, and lots of other tricks. You can also use it
as an actual debugger on MRI 1.9.2+ by installing [pry-debugger](https://github.com/nixme/pry-debugger).

[Learn more about YADR's pry customizations and how to install](https://github.com/skwp/dotfiles/blob/master/README-pry.md)

### Git 사용자 정보

gitconfig 자체가 사용자 정보를 담고있지 않기 때문에 환경변수를 사용할 것을 권한다. 아래 환경변수를 `~/.secrets` 파일에 넣어두면 zshrc 에서 참조할 것이다:

>    # git 사용자 정보를 넣어두셈  
>    export GIT_AUTHOR_NAME='Your Name'  
>    export GIT_AUTHOR_EMAIL='you@domain.com'  
>    export GIT_COMMITTER_NAME='Your Name'  
>    export GIT_COMMITTER_EMAIL='you@domain.com'  
>  
>    # 귀찮다면, GitHub 로그인 정보도 넣어두면 좋지  
>    export GITHUB_USER='your_user_name'  
>    export GITHUB_TOKEN='your_github_token'    
  

### Git 커스토마이징:

  * `git l` - a much more usable git log
  * `git b` - a list of branches with summary of last commit
  * `git r` - a list of remotes with info
  * `git t` - a list of tags with info
  * `git nb` - a (n)ew (b)ranch - like checkout -b
  * `git cp` - cherry-pick -x (showing what was cherrypicked)
  * `git changelog` - a nice format for creating changelogs
  * Some sensible default configs, such as improving merge messages, push only pushes the current branch, removing status hints, and using mnemonic prefixes in diff: (i)ndex, (w)ork tree, (c)ommit and (o)bject
  * Slightly improved colors for diff
  * `git unstage` (remove from index) and `git uncommit` (revert to the time prior to the last commit - dangerous if already pushed) aliases

### RubyGems

.gemrc 파일이 제공되는데,  매번 타이핑 안해도 기본으로 설정되어 있음:   
`gem install whatever --no-ri --no-rdoc`. `--no-ri --no-rdoc`

### 모든 것을 vim 방식으로!

The provided inputrc and editrc will turn your various command line tools like mysql and irb into vim prompts. There's
also an included Ctrl-R reverse history search feature in editrc, very useful in irb.

### Vim 환경설정

.vimrc 파일에 설명이 단위별로 잘 쪼개져 있으니 들여다보고 손수 고쳐서 사용하길 바람.


### Vim 키맵

vim/plugin/settings 아래 파일은 각각의 플러그인에 해당하는 설정파일들이다.  핵심  키맵파일은 skwp-keymap.vim 이지만 몇몇 vim 파일들도 키 맵핑 설정을 담고 있다. (그 설정들을 모두 skwp-keymap.vim 로 이동시킬 예정)

### vim 키 맵핑 디버깅

만약 동작이 이상해서 뭣 때문에 그런지 알수 있는 방법이 있다:  
`:map [keycombo]`  (예 `:map <C-\>`) 

키가 맵핑되어 있는 상태를 보여준다.  설정이 어디에 있는지도 알고싶다면 다음 명령을 해보라:  
`:verbose map [keycombo]`
  
keycombo를 생략하면 모든 맵을 리스팅 해준다. nmap, imap, vmap, 등등에도 마찬가지로 적용될 수 있다.


#### 커서 움직이기

 * `,z` - go to previous buffer (:bp)
 * `,x` - go to next buffer (:bn)
 * `Cmd-j` and `Cmd-k` to move up and down roughly by functions
 * `Ctrl-o` - Old cursor position - this is a standard mapping but very useful, so included here
 * `Ctrl-i` - opposite of Ctrl-O (again, this is standard)

#### LustyJuggler

 * `,lj` - show buffers (LustyJuggler buffer search), just type to fuzzy match a buffer name
 * `,lf` - file system browser

#### Rails

 * `Cmd-Shift-R` to use vim-ruby-conque to run a spec file. `Cmd-Shift-L` to run from a line (individual it block), `,Cmd-Shift-R` to rerun the last run command (great for re-running specs)
 * :Rspec1 and :Rspec2 to switch between rspec versions for the vim-ruby-conque runner
 * `,vv` and `,cc` to switch between view and controller

#### Surround.vim customizations

 * in plugin/settings/surround.vim (this folder contains all my customizations)
 * the `#` key now surrounds with `#{}`, so `ysaw#` (surround around word) `#{foo}`
 * `=` surrounds with `<%= erb tag %>`; `-` for `<% this %>`. So, `yss=` or `yss-` to wrap code

#### 검색하기 / 코드 찾기

 * `,f` - instantly Find definition of class (must have exuberant ctags installed)
 * `,F` - same as `,f` but in a vertical split
 * `,,f` - jump to Method. Same as vim's built in jump to tag, but much more aware of ruby bang_methods! and method.invocations!
 * `,,F` - same as `,,f` but in a vertical split
 * `,gf` or `Ctrl-f` - same as vim normal gf (go to file), but in a vertical split (works with file.rb:123 line numbers also)
 * `gF` - standard vim mapping, here for completeness (go to file at line number)
 * `K` - GitGrep the current word under the cursor and show results in quickfix window
 * `,K` - GitGrep the current word up to next exclamation point (useful for ruby foo! methods)
 * `Cmd-*` - highlight all occurrences of current word (similar to regular `*` except doesn't move)
 * `,hl` - toggle search highlight on and off
 * `,gg` - GitGrep command line, type between quotes
 * `,gd` - GitGrep def (greps for 'def [function name]') when cursor is over the function name
 * `,gcp` - GitGrep Current Partial to find references to the current view partial
 * `,gcf` - GitGrep Current File to find references to the current file
 * `//` - clear the search
 * `,q/` -  quickfix window with last search (stolen from Steve Losh)
 * `,qa/` - quickfix Ack last search (Steve Losh)
 * `,qg/` - quickfix GitGrep last search
 * `,T` - Tag list (list of methods in a class)
 * `Ctrl-s` - Open related spec in a split. Similar to :A and :AV from rails.vim but is also aware of the fast_spec dir and faster to type
 * `,,w` (alias `,<esc>`) or `,,b` (alias `,<shift-esc>`) - EasyMotion, a vimperator style tool that highlights jump-points on the screen and lets you type to get there.

#### 파일 네비게이션

 * `,t` - CtrlP fuzzy file selector
 * `,b` - CtrlP buffer selector
 * `Cmd-Shift-M` - jump to method - CtrlP tag search within current buffer
 * `,jm` jump (via CtrlP) to app/models
 * `,jc` app/controllers
 * `,jv` app/views
 * `,jh` app/helpers
 * `,jl` lib
 * `,jp` public
 * `,js` spec
 * `,jf` fast_spec
 * `,jt` test
 * `,jd` db
 * `,jC` config
 * `,jV` vendor
 * `,jF` factories
 * `Cmd-Shift-P` - Clear CtrlP cache
 * `:Bopen [gem name]` to navigate to a gem (@tpope/vim-bundler)

#### RSI-reduction

 * Cmd-Space to autocomplete. Tab for snipmate snippets.
 * `Cmd-k` and `Cmd-d` to type underscores and dashes (use Shift), since they are so common in code but so far away from home row
 * `Ctrl-l` to insert a => hashrocket (thanks @garybernhardt)
 * `,.` to go to last edit location (same as `'.`) because the apostrophe is hard on the pinky
 * `,ci` to change inside any set of quotes/brackets/etc
 * `,#` `,"` `,'` `,]` `,)` `,}` to surround a word in these common wrappers. the # does #{ruby interpolation}. works in visual mode (thanks @cj)
 * `Cmd-'`, `Cmd-"`, `Cmd-]`, `Cmd-)`, etc to change content inside those surrounding marks. You don't have to be inside them.

#### 탭 돌아다니기

 * `Ctrl-H` and `Ctrl-L` - left an right on tabs
 * Use `Cmd-1` thru `Cmd-9` to switch to a specific tab number (like iTerm) - and tabs have been set up to show numbers

#### 윈도우 돌아다니기

 * `Ctrl-h,l,j,k` - to move left, right, down, up between windows
 * `Q` - Intelligent Window Killer. Close window `wincmd c` if there are multiple windows to same buffer, or kill the buffer `bwipeout` if this is the last window into it.
 * Cmd-Arrow keys - resize windows (up/down for vertical, left=make smaller horizontally, right=make bigger horizontally)

#### 화면 나누기

 * `vv` - vertical split (`Ctrl-w,v`)
 * `ss` - horizontal split (`Ctrl-w,s`)
 * `,qo` - open quickfix window (this is where output from GitGrep goes)
 * `,qc` - close quickfix
 * `,gz` - zoom a window to max size and again to unzoom it (ZoomWin plugin, usually `C-w,o`)

#### NERDTree 프로젝트 트리

 * `Cmd-Shift-N` - NERDTree toggle
 * `Ctrl-\` - Show current file tree

#### Utility

 * `,orb` - outer ruby block. takes you one level up from nested blocks (great for rspec)
 * `crs`, `crc`, `cru` via abolish.vim, coerce to snake_case, camelCase, and UPPERCASE. There are more `:help abolish`
 * `:NR` - NarrowRgn - use this on a bit of selected text to create a new split with just that text. Do some work on it, then :wq it to get the results back.
 * `,ig` - toggle visual indentation guides
 * `,cf` - Copy Filename of current file (full path) into system (not vi) paste buffer
 * `,cn` - Copy Filename of current file (name only, no path)
 * `,vc` - (Vim Command) copies the command under your cursor and executes it in vim. Great for testing single line changes to vimrc.
 * `,vr` - (Vim Reload) source current file as a vim file
 * `,yw` - yank a word from anywhere within the word (so you don't have to go to the beginning of it)
 * `,ow` - overwrite a word with whatever is in your yank buffer - you can be anywhere on the word. saves having to visually select it
 * `,ocf` - open changed files (stolen from @garybernhardt). open all files with git changes in splits
 * `,w` - strip trailing whitespaces
 * `sj` - split a line such as a hash {:foo => {:bar => :baz}} into a multiline hash (j = down)
 * `sk` - unsplit a link (k = up)
 * `,he` - Html Escape
 * `,hu` - Html Unescape
 * `,hp` - Html Preview (open in Safari)
 * `Cmd-Shift-A` - align things (type a character/expression to align by, works in visual mode or by itself)
 * `:ColorToggle` - turn on #abc123 color highlighting (useful for css)
 * `:gitv` - Git log browsers
 * `,hi` - show current Highlight group. if you don't like the color of something, use this, then use `hi! link [groupname] [anothergroupname]` in your vimrc.after to remap the color. You can see available colors using `:hi`
 * `,yr` - view the yankring - a list of your previous copy commands. also you can paste and hit `ctrl-p` for cycling through previous copy commands

#### Ruby Debugger

 * Visual ruby debugger included. All keys remapped to `,d(something)` such as `,dn` for Debugger Next or `,dv` for Debugger Variables. Use `:help ruby-debugger` for more info, but keep in mind the new key maps (see vim/plugin/settings/vim-ruby-debugger.vim)

#### 주석

 * `Cmd-/` - toggle comments (usually gcc from tComment)
 * `gcp` (comment a paragraph)

 **Wrapping**

 * :Wrap - wrap long lines (e.g. when editing markdown files).
 * Cmd-[j, k, $, 0, ^] - navigate display lines.

### 배포본에 포함된 vim 플러그인

#### 네비게이션

 * NERDTree - 나 빼고 모두가 좋아하는 tree 브라우저
 * NERDTree-tabs - makes NERDTree play nice with MacVim tabs so that it's on every tab
 * ShowMarks - creates a visual gutter to the left of the number column showing you your marks
 * EasyMotion - hit ,<esc> (forward) or ,<Shift-Esc> (back) and watch the magic happen. Just type the letters and jump directly to your target - in the provided vimrc the keys are optimized for home row mostly. Using @skwp modified EasyMotion which uses vimperator-style two character targets.
 * LustyJuggler/Explorer - hit B, type buf name to match a buffer, or type S and use the home row keys to select a buffer
 * TagBar - hit ,T to see a list of methods in a class (uses ctags)
 * CtrlP - Ctrl-p or ,t to find a file

#### Git

 * fugitive - "a git wrapper so awesome, it should be illegal...". Try Gstatus and hit `-` to toggle files. Git `d` to see a diff. Learn more: http://vimcasts.org/blog/2011/05/the-fugitive-series/
 * gitv - use :gitv for a better git log browser
 * GitGrep - much better than the grep provided with fugitive; use :GitGrep or hit K to grep current word

#### 색상

 * AnsiEsc - inteprets ansi color codes inside log files. great for looking at Rails logs
 * solarized - a color scheme scientifically calibrated for awesomeness (including skwp mods for ShowMarks)
 * csapprox - helps colors to be represented correctly on terminals (even though we expect to use MacVim)
 * Powerline - beautiful vim status bar. Requires patched fonts (installed from fonts/ directory)

#### 코딩

 * tComment - gcc to comment a line, gcp to comment blocks, nuff said
 * sparkup - div.foo#bar - hit `ctrl-e`, expands into `<div class="foo" id="bar"/>`, and that's just the beginning
 * rails.vim - syntax highlighting, gf (goto file) enhancements, and lots more. should be required for any rails dev
 * rake.vim - like rails.vim but for non-rails projects. makes `:Rtags` and other commands just work
 * ruby.vim - lots of general enhancements for ruby dev
 * necomplcache - intelligent and fast complete as you type, and added Command-Space to select a completion (same as Ctrl-N)
 * snipMate - offers textmate-like snippet expansion + scrooloose-snippets . try hitting TAB after typing a snippet
 * jasmine.vim - support for jasmine javascript unit testing, including snippets for it, before, etc..
 * vim-javascript-syntax, vim-jquery - better highlighting
 * TagHighlight - highlights class names and method names
 * vim-coffeescript - support for coffeescript, highlighting
 * vim-stylus - support for stylus css language
 * vim-bundler - work with bundled gems
 * vim-ruby-debugger - visual IDE-style debugger. Use `:help ruby-debugger` or `:Rdebugger` and `,dn` to step

#### TextObjects

 The things in this section provide new "objects" to work with your standard verbs such as yank/delete/change/=(codeformat), etc

 * textobj-rubyblock - ruby blocks become vim textobjects denoted with `r`. try var/vir to select a ruby block, dar/dir for delete car/cir for change, =ar/=ir for formatting, etc
 * vim-indentobject - manipulate chunks of code by indentation level (great for yaml) use vai/vii to select around an indent block, same as above applies
 * argtextobj - manipulation of function arguments as an "a" object, so vaa/via, caa/cia, daa/dia, etc..
 * textobj-datetime - gives you `da` (date), `df` (date full) and so on text objects. useable with all standard verbs
 * vim-textobj-entire - gives you `e` for entire document. so vae (visual around entire document), and etc
 * vim-textobj-rubysymbol - gives you `:` textobj. so va: to select a ruby symbol. da: to delete a symbol..etc
 * vim-textobj-function - gives you `f` textobj. so vaf to select a function
 * next-textobject - from Steve Losh, ability to use `n` such as vinb (visual inside (n)ext set of parens)

#### Utils

 * SplitJoin - easily split up things like ruby hashes into multiple lines or join them back together. Try :SplitjoinJoin and :SplitjoinSplit or use the bindings sj(split) and sk(unsplit) - mnemonically j and k are directions down and up
 * tabularize - align code effortlessly by using :Tabularize /[character] to align by a character, or try the keymaps
 * yankring - effortless sanity for pasting. every time you yank something it goes into a buffer. after hitting p to paste, use ctrl-p or ctrl-n to cycle through the paste options. great for when you accidentally overwrite your yank with a delete.
 * surround - super easy quote and tag manipulation - ysiw" - sourround inner word with quotes. ci"' - change inner double quotes to single quotes, etc
 * greplace - use :Gsearch to find across many files, replace inside the changes, then :Greplace to do a replace across all matches
 * ConqueTerm - embedded fully colorful shell inside your vim
 * vim-ruby-conque - helpers to run ruby,rspec,rake within ConqueTerm
 * vim-markdown-preview - :Mm to view your README.md as html
 * html-escape - ,he and ,hu to escape and unescape html
 * ruby-debug-ide - not quite working for me, but maybe it will for you. supposedly a graphical debugger you can step through
 * Gundo - visualize your undos - pretty amazing plugin. Hit ,u with my keymappings to trigger it, very user friendly
 * slime - use ctrl-c,ctrl-c to send text to a running irb/pry/console. To start the console, you must use screen with a named session: "screen -S [name] [cmd]", ex: "screen -S pry pry"
 * vim-indent-guides - visual indent guides, off by default
 * color_highlight - use :ColorCodes to see hex colors highlighted
 * change-inside-surroundings - change content inside delimiters like quotes/brackets
 * Specky - used for color highlighting rspec correctly even if specs live outside of spec/ (rails.vim doesn't handle this)

#### General enhancements that don't add new commands

 * Arpeggio - allows you to define key-chord combinations
 * IndexedSearch - when you do searches will show you "Match 2 of 4" in the status line
 * delimitMate - automatically closes quotes
 * SearchComplete - tab completion in the / search window
 * syntastic - automatic syntax checking when you save the file
 * repeat - adds `.` (repeat command) support for complex commands like surround.vim. i.e. if you perform a surround and hit `.`, it will Just Work (vim by default will only repeat the last piece of the complex command)
 * endwise - automatically closes blocks (if/end)
 * autotag - automatically creates tags for fast sourcecode browsing. use ctrl-[ over a symbol name to go to its definition
 * matchit - helps with matching brackets, improves other plugins
 * sass-status - decorates your status bar with full nesting of where you are in the sass file


### vim 셋팅 덮어쓰기

You may use `~/.vimrc.before` for settings like the __leader__ setting.
You may `~/.vimrc.after` (for those transitioning from janus) or in `~/.yadr/vim/after/.vimrc.after` for any additional overrides/settings.
If you didn't have janus before, it is recommended to just put it in `~/.yadr/vim/after` so you can better manage your overrides.


### vim 플러그인 추가하기

YADR comes with a dead simple plugin manager that just uses git submodules, without any fancy config files.

    yav -u https://github.com/airblade/vim-rooter

플러그인 삭제는 지금 안돼 -__-), 곧 될 것임

   ydv -p airblade-vim-rooter

The aliases (yav=yadr vim-add-plugin) and (yuv=yadr vim-update-all-plugins) live in the aliases file.
You can then commit the change. It's good to have your own fork of this project to do that.


## 기타


### OSX Hacks
The osx file is a bash script that sets up sensible defaults for devs and power users
under osx. Read through it before running it. To use:

    ./osx

These hacks are Lion-centric. May not work for other OS'es. My favorite mods include:

  * Ultra fast key repeat rate (now you can scroll super quick using j/k)
  * No disk image verification (downloaded files open quicker)
  * Display the ~/Library folder in finder (hidden in Lion)


### 쓸만한 OSX 툴

 * NValt - Notational Velocity alternative fork - http://brettterpstra.com/project/nvalt/ - syncs with SimpleNote
 * Vimium for Chrome - vim style browsing. The `f` to type the two char alias of any link is worth it.
 * QuickCursor - gives you Apple-Shift-E to edit any OSX text field in vim.
 * brew install autojump - will track your commonly used directories and let you jump there. With the zsh plugin you can just type `j [dirspec]`, a few letters of the dir you want to go to.


### Credits

I can't take credit for all of this. The vim files are a combination of
work by tpope, scrooloose, and many hours of scouring blogs, vimscripts,
and other places for the cream of the crop of vim awesomeness.

 * http://ethanschoonover.com/solarized - a scientifically calibrated color scheme
 * https://github.com/astrails/dotvim
 * https://github.com/carlhuda/janus
 * https://github.com/tpope
 * https://github.com/scrooloose
 * https://github.com/kana
 * https://github.com/sorin-ionescu
 * https://github.com/nelstrom

And everything that's in the modules included in vim/bundle of course.
Please explore these people's work.


### Contributors

 * 초기 버전: @skwp
 * 자동 설치 및 마무리: @kylewest
 * oh-my-zsh에서 Presto로 변경: @JeanMertz


### 좀 더 알아보려면

원 저작자 블로그를 참조: http://yanpritzker.com

