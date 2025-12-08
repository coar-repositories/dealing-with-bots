# {{ site.Title }}

{{ with site.GetPage "section" "context"}}
		{{- print "# " .Title -}}
    {{- print .RawContent "\n" }}
{{ end }}

{{ with site.GetPage "section" "problem-statement"}}
    {{- print "# " .Title -}}
    {{- print .RawContent "\n" }}
{{ end }}

{{ with site.GetPage "section" "model"}}
    {{- print "# " .Title -}}
    {{- print .RawContent "\n" }}
{{ end }}

{{ with site.GetPage "section" "process"}}
    {{- print "# " .Title -}}
    {{- print .RawContent "\n" }}
		{{- range .RegularPages -}}
        {{- print "## " .Title -}}
        {{- print .RawContent "\n" }}
		{{- end -}}
{{ end }}

{{ with site.GetPage "section" "tools-and-strategies"}}
    {{- print "# " .Title -}}
    {{- print .RawContent "\n" }}
    {{- range .RegularPages -}}
        {{- print "## " .Title}}
        {{- print "\n" .Description }}
        {{- print "[See website for more details](" .Permalink ")\n\n" }}
    {{- end -}}
{{ end }}