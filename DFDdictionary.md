# Data Flow Diagaram Dictionary

#### External Entities:
######1. Corporate Manager-Internal corporate individuals who will be the recipients of the external software manifests. From these manifests, they can make corporately impactful decisions. However, these decisions are beyond the scope of the current system. 
######2. Exteranl Repository-External locations of source code. This could include public and private repositories outside of the control of the organization. This could also include software received via software supply chains. 
######3. Corporate Developer-Planning and execution of a wide range of strategies to meet specific organizational objectives. 
######4.National Vulnerability Database- Government repository of standards-based vulnerability information. The NVD is a product of the National Institute of Stands and Technology (NIST) Computer Security Division and is used by the U.S.
#### Data Stores:
######1.SPDX DB- This is the database that is going to store information about files (remember that files -> packages -> projects). This information is going to have to be stored in a standardized way.
######2. NIST CPE Information-
#### Processes:
######1.	Manage Code Information-
######2.	Manage Project Information- Received provided project information and assemble and return discovered software license, copyright, vulnerability, and weakness information. 
######3.	Manage CPE Information-
######4.	License Scanner-
######5.	Version Control/Build System-
#### Data Flows:
######1.	Source Query- Internally initiated request for external source
######2.	File – Source file 
######3.	Package – Source package comprised of one or more files 
######4.	File SHA1 – Hash of file (e.g. http://www.sha1-online.com/)
######5.	File SHA1 Response – A yes/no response as to whether or not the hash of a file exists in the database.
######6.	File Copyright/License + Info – For any file that does not have a SHA1 in the database (i.e. doesn’t exist), a new record is created for that file. 
######7.	Project Query – Request for software project (comprised of many packages). 
######8.	Project Info – Relevant information about a project. This includes copyright, license, and vulnerability information.


