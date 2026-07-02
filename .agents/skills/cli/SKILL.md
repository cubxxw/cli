```markdown
# cli Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill introduces the core development patterns and workflows for the `cli` Go codebase. You'll learn the project's coding conventions, how to contribute features or bugfixes with corresponding tests, and how to update documentation efficiently. This guide is designed for contributors aiming to maintain consistency and quality in the repository.

## Coding Conventions

- **File Naming:**  
  Use `snake_case` for all file names.
  ```
  registry.go
  install_test.go
  ```

- **Import Style:**  
  Use **relative imports** for referencing internal packages.
  ```go
  import "../utils"
  ```

- **Export Style:**  
  Use **named exports** for functions, types, and variables that should be accessible outside the package.
  ```go
  // Named export
  func InstallSkill(name string) error {
      // ...
  }
  ```

## Workflows

### Feature or Bugfix with Tests
**Trigger:** When adding a new feature or fixing a bug, and updating or adding corresponding tests.  
**Command:** `/new-feature-with-tests`

1. Edit or create implementation file(s) in the relevant `internal` or `pkg` directory.
   ```
   internal/skills/registry/registry.go
   pkg/cmd/skills/install/install.go
   ```
2. Edit or create corresponding test file(s) in the same directory.
   ```
   internal/skills/registry/registry_test.go
   pkg/cmd/skills/install/install_test.go
   ```
3. Ensure your commit message uses a relevant prefix (e.g., `fix:`, `feat:`) and is concise.
4. Run all tests to verify correctness.
5. Submit your changes for review.

**Example:**
```go
// internal/skills/registry/registry.go
func RegisterSkill(name string) error {
    // implementation
}

// internal/skills/registry/registry_test.go
func TestRegisterSkill(t *testing.T) {
    // test implementation
}
```

---

### Multi-Docs Update
**Trigger:** When fixing or improving documentation across several files at once.  
**Command:** `/update-multiple-docs`

1. Edit multiple documentation files (e.g., `README`, install guides) to fix errors or improve content.
   ```
   docs/install_linux.md
   docs/install_macos.md
   docs/install_windows.md
   ```
2. Commit all related documentation changes together, using the `docs:` prefix in your commit message.
3. Submit your changes for review.

**Example:**
```markdown
# Install on Linux

Updated instructions for clarity and accuracy.
```

## Testing Patterns

- **Test Files:**  
  Test files follow the `*_test.go` naming convention and are located alongside their implementation files.

- **Framework:**  
  No specific testing framework detected; standard Go testing is assumed.

- **Example:**
  ```go
  // pkg/cmd/skills/install/install_test.go
  func TestInstallSkill(t *testing.T) {
      // test logic
  }
  ```

## Commands

| Command                  | Purpose                                               |
|--------------------------|-------------------------------------------------------|
| /new-feature-with-tests  | Start a feature or bugfix with corresponding tests    |
| /update-multiple-docs    | Update multiple documentation files in one commit     |
```
