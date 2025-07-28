# 🌱 Terraform - Quick reference

## 🔧 Initialization & Setup
- `terraform init` — Initialize a working directory.
- `terraform init -upgrade` — Upgrade provider plugins to latest acceptable version.
- `terraform init -backend=false` — Skip backend configuration.
- `terraform version` — Show the current Terraform version.
- `terraform -help` — Display help for Terraform commands.
- `terraform providers` — Show providers required for configuration.

## 🧪 Planning
- `terraform plan` — Show changes Terraform will make.
- `terraform plan -out=tfplan` — Save the plan to a file.
- `terraform plan -var 'key=value'` — Pass variables via CLI.
- `terraform plan -target=resource.name` — Target a specific resource.

## 🚀 Apply & Deployment
- `terraform apply` — Apply infrastructure changes.
- `terraform apply tfplan` — Apply a saved plan.
- `terraform apply -auto-approve` — Skip approval prompt.
- `terraform apply -refresh=false` — Skip refreshing state before apply.

## 💥 Destroying Infrastructure
- `terraform destroy` — Destroy all managed infrastructure.
- `terraform destroy -target=resource.name` — Destroy a specific resource.
- `terraform destroy -auto-approve` — Destroy without prompt.

## 📦 State Management
- `terraform state list` — List all resources in state.
- `terraform state show resource.name` — Show details of a resource.
- `terraform state rm resource.name` — Remove resource from state.
- `terraform state mv old.name new.name` — Rename/move resource in state.
- `terraform state pull` — Download raw state from backend.
- `terraform state push` — Upload local state to remote.

## 🔁 Refresh & Import
- `terraform refresh` — Sync state with real-world resources.
- `terraform import resource.name id` — Import existing resources into Terraform.
- `terraform import -allow-missing-config` — Import without existing config.

## 📄 Output & Variables
- `terraform output` — Display all output variables.
- `terraform output var_name` — Show specific output value.
- `terraform output -json` — Show outputs in JSON.
- `terraform console` — Interactive console for testing expressions.
- `terraform validate` — Check configuration syntax/validity.

## 🔍 Debugging & Logging
- `terraform plan -detailed-exitcode` — Useful for CI, exit 0=no changes, 2=changes.
- `TF_LOG=DEBUG terraform apply` — Enable debug logging.
- `TF_LOG_PATH=log.txt terraform apply` — Save logs to file.
- `terraform graph` — Generate resource dependency graph.

## 🔐 Backends & Workspaces
- `terraform workspace list` — List workspaces.
- `terraform workspace new dev` — Create new workspace.
- `terraform workspace select dev` — Switch workspace.
- `terraform workspace delete dev` — Delete a workspace.
- `terraform workspace show` — Show current workspace.

## 🔍 Formatting & Linting
- `terraform fmt` — Format Terraform code.
- `terraform fmt -recursive` — Format all .tf files in subdirs.
- `terraform validate` — Syntax validation of config files.

## 🔄 Modules
- `terraform get` — Download modules.
- `terraform get -update` — Update modules.

## 🧼 Misc
- `terraform login` — Authenticate to Terraform Cloud/Enterprise.
- `terraform logout` — Remove saved credentials.
- `terraform config list` — Show CLI configuration.
