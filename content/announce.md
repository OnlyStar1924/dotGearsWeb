---
title: "announce"
date: 2020-12-29T15:43:10+07:00
draft: false
---
{{< rawhtml>}}
{{ define "header_css" }}{{ end }}

{{ define "main" }}

 
  <!-- <div align="center">
      <a href="/"> <img src="/img/home.png" alt=".GEARS Home" hspace="0" vspace="0" border="4"></a>
  </div> -->
  
  <div class="grid justify-center">

    <div class="col-span-3 lg:col-span-2 mb-3">
      <!-- <h2 class="text-4xl">{{ humanize  .Title }}</h2> -->
      {{if .IsHome}}
      {{.Scratch.Set "Paginator" (.Paginate (where .Site.RegularPages "Type" "in" site.Params.mainSections) (.Site.Params.paginator_pages) )}}
      <div align="center">
        <a href="/"> <img src="/img/home.png" alt=".GEARS Home" hspace="0" vspace="0" border="4"></a>
      </div>
      {{else}}
      <div align="center">
        <a href="/news/"> <img src="" alt=".GEARS News" hspace="0" vspace="0" border="4"></a>
      </div>
      {{.Scratch.Set "Paginator" .Paginator}}
      {{end}}
      {{$paginator:=(.Scratch.Get "Paginator")}}
      {{ range $paginator.Pages }}
      <a href="{{.RelPermalink}}">
        {{ .Render "summary" }}
      </a>
      {{ end }}
      {{ partial "paginator.html" . }}
    </div>
</div>

{{ end }}
{{< /rawhtml>}}