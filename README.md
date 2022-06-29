# AV20
Archive Directory Viewer 2.0 (1989)

Released by Derron Simon in 1988 and updated through early 1989.  Source code *was* released but I've been unable to find it.  If you have it, please share!

Here is the AV.DOC:

                           Archive Directory Viewer v2.00
                        Copyright (c) 1988-9 by Derron Simon

                                    Derron Simon
                                   14 Valley Road
                                Glen Mills, PA 19342

                               CompuServe: 72571,1524
                                   GEnie: D.SIMON





            DESCRIPTION

            AV shows the contents of archives generated with most
            popular archive/library programs.  AV supports archives
            created by ZOO (by Rahul Dhesi), PKPAK (by Phil Katz), ARC
            (SEA), PAK (NoGate Consulting), LU (by Thom Henderson), SQ
            (by a variety of authors), DWC (by Dean W. Cooper), and
            PKZIP (another by Phil Katz).

            FEATURES

            AV has the following secondary features:
                 - Ability to determine archive type by the file's
                   extension.
                 - Archive type can be specified on the command line for
                   archives with non-default extensions.
                 - AV supports wildcards and command line stringing.

            SYNOPSIS

            AV is used as follows:

                 av [-alqzdp] filename[.ext] ...

                 "[-alqzdp]" specifies the archive type if it cannot be
                 determined by the archives extension.  All files on the
                 command line are treated as the type specified.  The
                 letters correspond to ARC/PAK/PKA, LBR, ?Q?, ZOO, DWC,
                 and ZIP files respectively.

                 "filename[.ext]" is the filename of the archive to
                 view.  If no extension and no archive type identifier
                 are supplied, AV defaults to ".ARC", if no extension is
                 given and a type is specified, AV uses the default
                 extension for that archiver.  Filenames may contain
                 wildcards and may be strung.  Note: there is no default
                 extension for squeezed files.

            OUTPUT

            AV's standard output is in the form:

                 AV copyright notice

                 file1.ext
                   contents

                 file2.ext
                   contents

                 .
                 .
                 .
            





                 filen.ext
                   contents

            The listing format is the same for DWC, ZOO, ARC, and ZIP
            files.


            AV uses the following terms when displaying files:

                 Filename - The name of the file in the archive.

                 Length - The length of the file before storing.

                 Method - The method used to store the file.  Different
                      archive programs have different names for the same
                      compression methods.  AV tries to use the name
                      used by the archive program which created each
                      archive.

                 SF - The storage factor achieved by the compression.

                 Size - The size of the compressed file.

                 Date - The date of the file before storing.

                 Time - The time of the file before storing.

                 CRC - Cyclic Redundancy Check on the file, taken before
                      storing with squeezed (?q?) files and after with
                      all others.  CRC-16 is used by all the programs
                      except ZIP which uses CRC-32.

            COMPILATION INFORMATION

            AV was compiled with Microsoft C v5.1 and linked with
            Microsoft LINK v3.65.  The editor used when writing AV was
            EC by C Source and the debugger was CodeView by Microsoft.

            ACKNOWLEDGEMENTS

            The following references were used in the creation and later
            versions of AV.

                 ARC.DOC by System Enhancements Associates (description
                 of what the archive bits mean, from 5.32 docs).

                 TM0401.TXT by System Enhancements Associates
                 (information on what's new in version 6.0 of ARC).

                 LUDEF5.DOC by Gary P. Novosielski (LBR header
                 information).

                 LU.ARC by Thom Henderson (implementation of LBR header
                 viewer and more widely used header format than





                 LUDEF5.DOC).

                 ARCVIEW.ARC by Doug Boone (another similar utility with
                 C source which shows ARC/PAK/DWC/ZOO files).

                 SQ.C86 by Richard Greenlaw (?Q? file header
                 information).

                 DWC Prototype A2 by Dean W. Cooper (another archive
                 utility which I found on GEnie with C source).

                 APPNOTE.TXT by Phil Katz (ZIP file header information).

                 ZIPVINC.ARC by Ken Brown (ZIP file viewer).

            TRADEMARKS

            ARC is a trademark of System Enhancements Associates.
            Microsoft C, LINK, and CodeView are trademarks of Microsoft
            Corporation.

            DISCLAIMER

            The author makes no claims to any responsibility whatsoever
            for any damage this program causes or is involved in.  I
            don't expect it will cause damage, but I can't guarantee it.

            VERSION INFORMATION

            Vers    Date    Description
            ----  --------  --------------------------------------------
            1.00  12/22/88  Read only single ARC files
            1.01  12/22/88  Showed multiple files with wildcards
            1.10  12/23/88  Added LBR support
            1.11  12/27/88  Added SQ support
            1.20* 12/27/88  Added support for ZOO files
            1.21  12/29/88  Fixed ZOO CRC error
            1.22  12/29/88  Fixed ZOO length<->size error
            1.23  12/29/88  Made ARC CRC in caps and added 0-filling
            1.24  12/29/88  Fixed options error-checking
            1.30* 12/29/88  Added SF output
            1.31  02/14/89  Fixed bug in extension checking
            1.32  02/16/89  Fixed divide by zero bug on zero length
                            files
            1.40  02/16/89  Added DWC support
            1.41  02/18/89  Fixed bugs created by versions 1.30 to 1.40
            1.42* 02/19/89  Added size for SQ files
            1.50  03/04/89  Added ZIP support
            1.90  03/17/89  Cleaned up main code (smaller EXE)
            1.91  03/18/89  Added subdir support for ARC v6.00 files
            1.92  03/18/89  Fixed ..\filename.ext problem
            2.00* 03/18/89  New Documentation and other small stuff

            * publicly released versions






            I am attempting to keep the number of versions of AV down to
            a minimum, if you need something please get in touch with me
            and I may be able to give a private version (my most recent,
            which isn't necessarily the publics most recent.

            FUTURE DIRECTIONS

            The following are on my agenda:

                 - Change the user interface to something more intuitive
                 - Add all new archive formats
                 - Create a library of routines to get info from
                   archives that is linkable to C (for BBS and utility
                   writers).

            COPYRIGHT

            AV is copyrighted by Derron Simon.  It is not in the public
            domain, but may be copied freely and distributed freely.  I
            retain exclusive rights to the program except the right to
            distribute and copy, which I retain but also extend to
            everyone.
