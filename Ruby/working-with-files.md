### Files

*Writing to a file*
f = File.new("./my_file.txt", "w")
f.puts ("This is a my file")
f.puts ("This is a second line!")
f.close

-------A slightly different way to read from a file-------

lines = ["This is a line", "This is a second line", "This is a third line"]

f = File.new("./my_file.txt", "w")
lines.each { |line| f.puts(line) }
f.close

--------------------------------------------

*Reading files*

lines = []

file = File.open("./sample.txt", "r")

while (line = file.gets)
	lines << line
end

file.close

lines.each { |line| puts line }