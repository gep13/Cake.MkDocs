<div class="mermaid">
graph TD;
Run-Integration-Tests-->Default;
Run-Integration-Tests-->Run-Integration-Tests-Standalone;
Default-->Package;
Package-->Export-Release-Notes;
Package-->Analyze;
Package-->Test;
Package-->Create-NuGet-Packages;
Package-->Create-Chocolatey-Packages;
Package-->DotNetCore-Pack;
DotNetCore-Pack-->DotNetCore-Build;
DotNetCore-Build-->Clean;
DotNetCore-Build-->DotNetCore-Restore;
Clean-->Show-Info;
Clean-->Print-AppVeyor-Environment-Variables;
Test-->DotNetCore-Test;
DotNetCore-Test-->Install-OpenCover;
Install-OpenCover-->Install-ReportGenerator;
Analyze-->DupFinder;
Analyze-->InspectCode;
Analyze-->CreateIssuesReport;
</div>
