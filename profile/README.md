<p align="center"><img src="https://raw.githubusercontent.com/broodforced/.github/main/assets/broodforced.png" width="128" alt="broodforced"></p>

<h1 align="center">broodforced</h1>

<p align="center">
  <em>Reconnaissance tools for authorized bug-bounty work. Small, quiet, and run anywhere.</em>
</p>

<p align="center">
  <sub>
    <a href="#cicada">cicada</a> &nbsp;·&nbsp;
    <a href="#tymbal">tymbal</a> &nbsp;·&nbsp;
    <a href="#philosophy">philosophy</a>
  </sub>
</p>

<br>

Two tools that work the recon side of a bug-bounty flow, sharing one JSON schema so data moves
cleanly between them. Cicada does the deep, machine-heavy pass on a workstation; Tymbal does the
first lightweight pass on anything that runs a shell.

<table>
  <tr>
    <td width="130" align="center"><sub>— I —</sub></td>
    <td>
      <b><a href="https://github.com/broodforced/cicada">cicada</a></b><br>
      <sub>Python. The recon → probe → report pipeline: subdomain enum, live probing, endpoint
      discovery, nuclei, JS analysis, fuzzing and secret detection, then a single-file dark HTML
      report plus HackerOne submission templates. Or, as the README puts it, it runs the tedious
      parts so you can do the thinking.</sub>
    </td>
  </tr>
  <tr>
    <td align="center"><sub>— II —</sub></td>
    <td>
      <b><a href="https://github.com/broodforced/tymbal">tymbal</a></b><br>
      <sub>POSIX shell (plus an optional Go build). Subdomain enum, HTTP probing, port scanning,
      basic header/CORS checks — no Python, no Go runtime required. Runs on Alpine, iSH on an
      iPhone, a Pi, a toaster with busybox. Feed its JSON to cicada when you get home.</sub>
    </td>
  </tr>
</table>

<br>

<p align="center"><sub>— —</sub></p>

## Philosophy

- **Run anywhere.** Tymbal is a shell script on purpose; cicada needs only a Python and a PATH.
- **Orchestrate, don't replace.** These tools surface the attack surface. They do not find bugs
  for you — you still verify, understand, and responsibly report.
- **One schema.** Both emit the same JSON shape, deduped, so results merge without fuss.
- **No Kali required.** Works on stock macOS and Linux.

<br>

<p align="center"><sub><code>broodforced</code> — a brood is the cohort of periodical cicadas that
emerges together; forced, because we like it that way (and, yes, it's a riff on
brute-forced).</sub></p>