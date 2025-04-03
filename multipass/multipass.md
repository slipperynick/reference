# Multipass Command Reference

## Instance Management
- **List Instances**  
  `multipass list`
- **Launch a New Ubuntu Instance**  
  `multipass launch`
- **Launch an Instance with a Specific Name**  
  `multipass launch --name <name>`
- **Open a Shell Session in an Instance**  
  `multipass shell <name>`
- **Execute a Command in an Instance**  
  `multipass exec <name> -- <command>`
- **Stop an Instance**  
  `multipass stop <name>`
- **Start a Previously Stopped Instance**  
  `multipass start <name>`
- **Delete an Instance (Must Be Stopped First)**  
  `multipass delete <name>`
- **Permanently Remove Deleted Instances and Their Data**  
  `multipass purge`
- **Display Detailed Information About an Instance**  
  `multipass info <name>`
- **Restart an Instance**  
  `multipass restart <name>`
- **Suspend an Instance**  
  `multipass suspend <name>`
- **Recover a Deleted Instance (If Not Purged)**  
  `multipass recover <name>`

## File & Network Management
- **Mount a Directory from Host to Instance**  
  `multipass mount <host-path> <name>`
- **Unmount a Previously Mounted Directory**  
  `multipass unmount <name>`
- **List Available Networks**  
  `multipass networks`
- **Transfer Files Between Host and Instance**  
  `multipass transfer <src> <dest>`

## Configuration & Settings
- **Set a Configuration Option**  
  `multipass set <key=value>`
- **Retrieve the Value of a Configuration Option**  
  `multipass get <key>`

## Image & Resource Management
- **List Available Images for Launching Instances**  
  `multipass find`
- **Launch an Instance with a Specific Image**  
  `multipass launch <image>` (e.g., `multipass launch 22.04`)
- **Launch an Instance with Specific CPUs and Memory Allocation**  
  `multipass launch --cpus <n> --mem <m>`

## Miscellaneous
- **Display the Installed Version of Multipass**  
  `multipass version`
- **Display Help for All Commands or a Specific Command**  
  `multipass help`
- **List Aliases for Commonly Used Commands**  
  `multipass aliases`

