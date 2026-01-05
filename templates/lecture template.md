<%*
let title = tp.file.title;

if (title.startsWith("Untitled")) {
  title = await tp.system.prompt("Title");
  await tp.file.rename(title);
}

let created = tp.date.now("dddd Do MMMM YYYY HH:mm");
let last_modified = await tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm") || created;

let frontmatter = `---\n`;
frontmatter += `title: ${title}\n`;
frontmatter += `created: ${created}\n`;
frontmatter += `last_modified: ${last_modified}\n`;
frontmatter += `aliases: []\n`;
frontmatter += `tags: []\n`;
frontmatter += `course: []\n`;
frontmatter += `LEC: []\n`;
frontmatter += `---\n`;

tR = frontmatter;
%>
