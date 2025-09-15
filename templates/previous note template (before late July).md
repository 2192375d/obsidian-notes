<%*
let title = tp.file.title;

if (title.startsWith("Untitled")) {
  title = await tp.system.prompt("Title");
  await tp.file.rename(title);
}

let frontmatter = ``
frontmatter += `---\n`;
frontmatter += `title: ${title}\n`;
frontmatter += `created: Before 29th July, 2025\n`; 
frontmatter += `last_modified: ${tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm")}\n`;
frontmatter += `tags: []\n`;
frontmatter += `course: []\n`;
frontmatter += `LEC: []\n`;
frontmatter += `---\n`;

tR += frontmatter;
%>
