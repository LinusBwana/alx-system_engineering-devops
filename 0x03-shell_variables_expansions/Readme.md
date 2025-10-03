Dangerous Shell Alias - Educational Documentation
⚠️ WARNING: DESTRUCTIVE SCRIPT
This document describes a highly dangerous shell script that should NEVER be used in production environments.
What This Script Does
The script creates a shell alias that replaces a common command with rm *, which deletes all files in the current directory.
Technical Details
bash# Conceptual structure (DO NOT EXECUTE):
alias <command_name>='rm *'
Why This Is Dangerous

Silent Data Destruction: Users executing what they think is a harmless command will unknowingly delete all files
No Recovery: Deleted files are typically unrecoverable without backups
Trust Exploitation: Exploits user trust in common commands
Cascading Damage: Could affect multiple directories if used repeatedly

Attack Vector
This is a classic example of:

Command substitution attack
Social engineering (tricking users to source the script)
Malicious shell configuration

How to Protect Yourself
Detection
Check your aliases:
bashalias                    # List all current aliases
type <command>           # Check if a command is aliased
which <command>          # Show command path
\<command>               # Bypass alias (use backslash)
Prevention

Never source untrusted scripts
Review alias definitions in your shell configuration files:

~/.bashrc
~/.bash_profile
~/.zshrc


Use absolute paths for critical operations
Enable shell safety features:

bash   set -o noclobber    # Prevent file overwriting
   alias rm='rm -i'    # Make rm interactive by default
Removal
If you've accidentally sourced this script:
bashunalias <command_name>   # Remove the dangerous alias
source ~/.bashrc         # Reload clean configuration
Educational Use Cases
This example is useful for teaching:

Shell security fundamentals
Social engineering awareness
System administration best practices
Incident response procedures
Security auditing techniques

Legitimate Alternatives
If you need to demonstrate this concept safely:
bash# Safe educational demo
alias ls='echo "⚠️  DEMO: This would delete files with rm *"'
Legal and Ethical Considerations

Unauthorized use is illegal in most jurisdictions
Violates computer fraud and abuse laws
Can result in criminal charges and civil liability
Only use in isolated, controlled environments with explicit permission

References

Shell scripting security best practices
OWASP Command Injection Prevention
System hardening guidelines
Incident response procedures


Remember: The purpose of understanding dangerous scripts is to defend against them, not to deploy them.