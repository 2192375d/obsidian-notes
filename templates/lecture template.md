<%*
let title = tp.file.title;

if (title.startsWith("Untitled")) {
  title = await tp.system.prompt("Title");
  await tp.file.rename(title);
}

// Start building YAML frontmatter
let frontmatter = `---\n`;
frontmatter += `title: ${title}\n`;
frontmatter += `created: ${tp.date.now("dddd Do MMMM YYYY HH:mm")}\n`;
frontmatter += `last_modified: ${tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm")}\n`;
frontmatter += `aliases: []\n`;
frontmatter += `tags: []\n`;
frontmatter += `course: []\n`;
frontmatter += `LEC: []\n`;
frontmatter += `---\n`;
tR += frontmatter;
%>