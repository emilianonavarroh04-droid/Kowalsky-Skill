# CLAUDE.md - Kowalsky OmniRoute Skills

This project contains OmniRoute Agent Skills integrated into the Kowalsky project.

## Project Structure

- `skills/` - OmniRoute agent skills (API and CLI)
  - Each skill is a directory containing a `SKILL.md` manifest file
  - Skills are drop-in documentation for AI agents to consume OmniRoute capabilities
  - 44 total skills across API and CLI categories

## Skill Categories

### API Skills (23)

Entry points for REST API access. Start with:
- `skills/omni-auth/SKILL.md` - Authentication and Bearer token management

### CLI Skills (21)

Entry points for CLI access. Start with:
- `skills/cli-serve/SKILL.md` - Server startup and management

## Development Notes

- Skills are read-only documentation manifests
- Manifests are auto-generated from OmniRoute source
- Do not manually edit skill manifests
- To update skills, re-sync from the main OmniRoute repository

## Integration Points

Skills can be consumed by:

1. **Claude Code** - Load skills via the `/skill` command
2. **MCP Tools** - Use `omniroute_agent_skills_list` MCP tool
3. **A2A Protocol** - Call `list-capabilities` JSON-RPC endpoint
4. **Direct URLs** - Reference manifests at:
   ```
   https://raw.githubusercontent.com/diegosouzapw/OmniRoute/main/skills/<id>/SKILL.md
   ```

## Git Workflow

- Work on feature branches (branch name: `claude/omniroute-skill-*`)
- Keep skill manifests synchronized with upstream OmniRoute
- Commit changes with clear, descriptive messages
- Push to the designated feature branch

## References

- **OmniRoute Repository**: https://github.com/diegosouzapw/OmniRoute
- **Skills Documentation**: See `skills/README.md`
- **OmniRoute Docs**: https://omniroute.dev/docs
