<%*
let title = tp.file.title;

if (title.startsWith("Untitled")) {
  title = await tp.system.prompt("Title");
  await tp.file.rename(title);
}

let frontmatter = ``
frontmatter += `---\n`;
frontmatter += `title: ${title}\n`;
frontmatter += `created: ${tp.date.now("dddd Do MMMM YYYY HH:mm")}\n`;
frontmatter += `last_modified: ${tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm")}\n`;
frontmatter += `aliases: []\n`;
frontmatter += `tags: [music/theory]\n`;
frontmatter += `course: MUZB80\n`;
frontmatter += `---\n`;

tR += frontmatter;
%>