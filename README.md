# Remove-Paragraph-Tags-From-Images-in-WordPress




function filter_ptags_on_images($content){
    return preg_replace('/
\s*(<a>)?\s*(<img alt="" />)\s*(&lt;\/a&gt;)?\s*&lt;\/p&gt;/iU', '\1\2\3', $content);
}
add_filter('the_content', 'filter_ptags_on_images');</a>
