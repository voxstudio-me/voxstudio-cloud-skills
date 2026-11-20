# VoxStudio Cloud Agent Skills

Use [VoxStudio on the web](https://voxstudio.me) from Cursor and other Agent Skills clients that support remote HTTP MCP with OAuth.

| Skill | What it does |
| --- | --- |
| [voxstudio-cloud-connect](skills/voxstudio-cloud-connect/SKILL.md) | Connect Cursor and verify access to the Cloud library |
| [voxstudio-recording-qa](skills/voxstudio-recording-qa/SKILL.md) | Search recordings, verify transcript passages, and cite sources |
| [voxstudio-transcribe](skills/voxstudio-transcribe/SKILL.md) | Transcribe audio or video and optionally translate subtitles |
| [voxstudio-voiceover](skills/voxstudio-voiceover/SKILL.md) | Turn a script into audio with an available reference voice |
| [voxstudio-media-export](skills/voxstudio-media-export/SKILL.md) | Preview sessions and export transcripts, subtitles, or audio |

## Install in Cursor

Run this from the project where you want to use the skills.

```sh
npx skills add voxstudio-me/voxstudio-cloud-skills -a cursor
```

You can also copy the desired skill directories into `.cursor/skills/` in your project. Open a new Cursor chat and type `/` to find the skills.

In VoxStudio, open **Settings → MCP → Cursor** and use the installation link. For manual configuration, merge the following entry into Cursor's MCP config.

```json
{
  "mcpServers": {
    "voxstudio-cloud": {
      "url": "https://voxstudio.me/cloud/mcp"
    }
  }
}
```

Select **Authenticate** if prompted and complete the VoxStudio browser consent flow. The skills use the tools advertised by the Cloud connection. Transcription and voiceover can create Cloud jobs and consume account credits.

## License

[MIT](LICENSE)
