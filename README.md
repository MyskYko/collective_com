# collective_com

Everything is written in C++.
"src" is source directory, "include" is include directory.
All the other directories are testcase. Note that some testcases are outdated and not able to be synthesized.

This program requires "ABC". https://people.eecs.berkeley.edu/~alanmi/abc/
Complile ABC and set PATH to the directory of ABC. (export PATH=$PATH:"where ABC is")

"make" this program before using. Executable will be generated as "/bin/gen".

For example, move to one of the directories of testcase.
Type "../bin/gen setting.txt out.blif"
It generates out.blif which is dataflow(expressed in BLIF).

Graphing tool is "dotgen.cpp". You can compile as "g++ dotgen.cpp -o dotgen".
Type "./dotgen out.blif out.png". It generates dataflow png in "out.png".

"mesh.cpp" is also for graphing. It generates intermediate file which is used by python codes.
Hard to explain to use, please compile program "g++ meshgen.cpp -o meshgen" and use shell scripit "ring.sh" for 4 ring connected environment or "mesh.sh" for 4x4 mesh connected environment. It is assumed these shell scripts are called from the directory of testcase like "../mesh.sh out.blif 4". It requires the number of cycles (= the number of step + 1).

For more details, please ask me. 
