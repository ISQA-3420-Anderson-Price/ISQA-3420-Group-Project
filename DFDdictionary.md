# Data Flow Diagaram Dictionary

#### External Entities:
 - Community - The open source community whos code is being used by the company.
 - Corporate Developer - Planning and execution of a wide range of strategies to meet specific organizational objectives. 
 - Corporate Manager - Internal corporate individuals who will be the recipients of the external software manifests. From these manifests, they can make corporately impactful decisions. However, these decisions are beyond the scope of the current system. 
 - External Repository - External locations of source code. This could include public and private repositories outside of the control of the organization. This could also include software received via software supply chains.
 - National Vulnerability Database - Government repository of standards-based vulnerability information. The NVD is a product of the National Institute of Stands and Technology (NIST) Computer Security Division and is used by the U.S.

#### Data Stores:
 - NIST CPE Information- CPE is a structured naming scheme for information technology systems, software, and packages.
 - SPDX DB- This is the database that is going to store information about files (remember that files -> packages -> projects). This information is going to have to be stored in a standardized way.

#### Processes:
 - CVE Lookup - Takes the CPE information for a package and sends it in a request to the National Vulnerablities Database to retieve CVE data.
 - License Scanner - The process of receiving a file/package and responding with specific license information.
 - Manage Code Information - The process of handling changes to computer code. Management of code modules or collections of lines of code in order to support changes to particular goals such as maintenance to a system.
 - Manage CPE Information - Ability to manage applications, operating systems, and hardware devices by describing and identifying classes. 
 - Manage Project Information - Received provided project information and assemble and return discovered software license, copyright, vulnerability, and weakness information. 
 - Policy Comparison - Compares a package to a policy to provide feedback to the corporate manager.
 - Version Control/Build System - The process of receiving a file/package developing this file and submitting it to be Managed code information.

#### Data Flows:
 - Comparison Response - In this context, the comparison response is the result returned to the manager after the Policy Comparison process finishes comparing project info to a policy.
 - CPE Info - Common Platform Enumeration information
 - CPE Request - Request to National Vulnerability Database for CPE data using the package name.
 - CPE Response - Response from the National Vulnerabilities Database including the CPE Info
 - CVE Request with CPE - Request for CVE information using CPE
 - CVE Info - Common vulnerabilities and exposures information
 - File - Source file 
 - File Copyright/License + Info – For any file that does not have a SHA1 in the database (i.e. doesn’t exist), a new record is created for that file. 
 - File SHA1 – Hash of file (e.g. http://www.sha1-online.com/)
 - File SHA1 Response – A yes/no response as to whether or not the hash of a file exists in the database.
 - License Info - License information returned from the License scanner.
 - License and Vulnerabilities Info - Information retrieved from the License Scanner and the National Vulnerabilites Database 
 - Package – Source package comprised of one or more files
 - Package Name - Unique name of a package used to lookup CPE information
 - Policy Comparison Request w/ Project Info - A request from the manager to initiate the Policy Comparison process.
 - Policy Info - The details of a policy definition including the warning and restriction levels or criteria for licenses and vulnerabilities.
 - Policy Request - A request to the SPDX Database by the Policy Comparison process for policy info.
 - Project File - File containing project info provided by the developer.
 - Project Info - Relevant information about a project. This includes copyright, license, and vulnerability information.
 - Project Info Request - Request for software project (comprised of many packages).
 - Project Info Response - A response to a project info request including the project info.
 - Modified Package - Represents a package that has been modified by the company and are going to be returned to the open source community if the license requires it.
 - Notice to Publish Modified Code to Community - A notification from the manager to the developer to release modified packages and files to the open source community.
 - Source Query - Internally initiated request for external source.
