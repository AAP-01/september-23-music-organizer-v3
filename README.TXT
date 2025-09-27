Project: music-organizer-v3. A project to collect audio files.
Authors: David J. Barnes and Michael Kölling

This project is part of the material for the book

   Objects First with Java - A Practical Introduction using BlueJ
   Seventh edition
   David J. Barnes and Michael Kölling

It is discussed in chapter 4.

To start:

Create a MusicOrganizer object on the object bench.
Use its methods to add, remove, and play files. The listAllFiles
method prints a list of the collection.

Lab 4#
21. calling listAllFiles() does indeed print the 3 files i've inputted in 
addFile(String filename)
22. x
23. with the breakpoint set on the loop body of listAllFiles(), the 
debugger shows that the method will print a file every time once it passes 
the loop body, and then it goes back to the beginning
24. listWithIndex method
    public void listWithIndex()
    {
        int position = 0;
        for(String filename : files) {
            System.out.println(position + ": " + filename);
            position++;
        }
    }

25. listMatching method
    public void listMatching(String searchString)
    {
        for(String filename : files) {
            if(filename.contains(searchString)){
                System.out.println(filename);
            }
        }
    }
if i type a string that does exist in the collection, it'll print the string. if not, nothing 
will happen.

26. updated listMatching method
    public boolean listMatching(String searchString)
    {
        boolean fileMatch = false;
        for(String filename : files) {
            if(filename.contains(searchString)){
                System.out.println(filename);
                fileMatch = true;
            }
            else {
                System.out.println("There is no file matching the input.");
                fileMatch = false;
            }
        }
        return fileMatch;
    }
note that if there are no items in the collection, the else statement will print nothing 
there is nothing

27. playSamplesByArtist method
    public void addFile(String filename, String artistName)
    {
        files.add(filename +" by " + artistName);
    }
...
    public boolean listMatching(String searchString)
    {
        boolean fileMatch = false;
        for(String filename : files) {
            if(filename.contains(searchString)){
                System.out.println(filename);
                fileMatch = true;
            }
            else {
                System.out.println("There is no file matching the input.");
                fileMatch = false;
            }
        }
        return fileMatch;
    }

28. for(Track track : tracklist)