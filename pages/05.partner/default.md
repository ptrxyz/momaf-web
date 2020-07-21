---
title: Partner
media_order: 'pk01.css,20171024_DigitalBW_LOGO_RGB_RZ.png,BW100_GR_4C_MWK_WEISS.png'
process:
    twig: true
    markdown: false
visible: true
admin:
    children_display_order: default
content:
    items: '@self.children'
---

{% do assets.addCss('page://05.partner/pk01.css') %}

{% for p in page.collection %}
{% set section = p.contentMeta.shortcodeMeta.shortcode.section %}
<table class='panel'>
    <tr>
        <td class='clogo' rowspan=3>{{ section.logo }}</td>
        <td class='cinstitute'>{{ section.institute }}</td>
    </tr>
    <tr>
        <td class='cdescription'>{{ section.description }}</td>
    </tr>
    <tr>
        <td class='ccontact'>
        {{ section.website }}
        {{ section.contact }}
        </td>
    </tr>
</table>

{% endfor %}

Sponsored by:  
[![](BW100_GR_4C_MWK_WEISS.png?resize=300,200)](https://mwk.baden-wuerttemberg.de/de/startseite/)
[![](20171024_DigitalBW_LOGO_RGB_RZ.png?resize=300,200)](https://www.digital-bw.de/)