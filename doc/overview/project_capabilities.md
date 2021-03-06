Project Capabilities
=============================================

Please read [about project capabilities](about_project_capabilities.md).

Below is a section for each project capability to describe itself including
what it semantically is intended to mean possibly including examples of projects
known to declare the capability.

| Project capability | Description |
| ------------------ | ----------- |
| VisualC | Project may contain or compile C++ source files.
| CSharp | Project may contain or compile C# source files.
| VB | Project may contain or compile VB source files.
| CPS | Project is based on the Project System Extensibility SDK
| HostSetActiveProjectConfiguration
| ProjectConfigurationsInferredFromUsage
| ProjectConfigurationsDeclaredAsItems
| RunningInVisualStudio
| NotLoadedWithIDEIntegration
| RenameNearbySimilarlyNamedImportsWithProject
| DeclaredSourceItems
| UserSourceItems
| SourceItemsFromImports
| AssemblyReferences | Indicates that the project supports assembly references.
| COMReferences | Indicates that the project supports COM references.
| ProjectReferences | Indicates that the project supports project references.
| SDKReferences
| SharedProjectReferences | Indicates that the project supports references to Shared Projects.
| WinRTReferences
| OutputGroups
| AllTargetOutputGroups
| VisualStudioWellKnownOutputGroups
| SingleFileGenerators
| Managed
| SharedAssetsProject
| SharedImports
| NestedProjects
| WindowsXaml
| WindowsXamlPage
| WindowsXamlCodeBehind
| WindowsXamlResourceDictionary
| WindowsXamlUserControl
| RelativePathDerivedDefaultNamespace | *DEPRECATED* This is an example of a BAD project capability because it merely exists to activate a design-time experience and does not reflect a genuine capability of the project.  This should be a project property instead.
| ReferencesFolder | *DEPRECATED* This is an example of a BAD project capability because it merely exists to activate a design-time experience and does not reflect a genuine capability of the project.  If worth keeping at all, this should be a project property instead.
| LanguageService | *DEPRECATED* This is an example of a BAD project capability because it merely exists to activate a design-time experience and does not reflect a genuine capability of the project.  If worth keeping at all, this should be a project property instead.
| BuildWindowsDesktopTarget
| PerPlatformCompilation (aka. #ifdef capability) | Indicates that items in this project are compiled individually for every target platform.
| MultiTarget | Indicates that items in this project may be applied to multiple platforms.

## Summary table

Below is a table that summarizes each capability and popular project types
they are declared in:

| Legend |                                                                                        |
|:------:|----------------------------------------------------------------------------------------|
|   U    | Unconfigured Project scope (capabilities appear in Unconfigured and Configured scopes) |
|   C    | Configured Project scope only                                                          |
|  Bold  | already shipped                                                                        |

## Additional discussion

#### PerPlatformCompilation

Defined by: Shared projects 

Summary: Indicates that items in this project are compiled individually
for every target platform.

What about when/if XAML gains the ability to have per-platform (or
per-form factor) XAML sections? This might be done at runtime or
compile time perhaps. We might want to upfront define whether either
of these future mechanisms would merit this capability or a new one.

Answer: PerPlatformXamlCompilation may come later.
    
#### MultiTarget (aka. Multiplat capability)

Defined by: PCLs and Shared Projects

Summary: Indicates that items in this project may be applied to multiple
platforms.

This capability is only present for PCLs that actually target > 1
platform (not a PCL that targets 1).

