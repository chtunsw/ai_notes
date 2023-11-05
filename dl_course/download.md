# Download assignments from Coursera Deep Learning Course

# Steps

1. Go to the home of the coursera-notebook hub

2. Create a new python notebook

3. Execute following in a cell

```bash
!tar cvfz allfiles.tar.gz *
```

4. Download the archive

If the resulting archive is too big and you can't download it

1. Open the python notebook where you executed last command and execute the following in a cell:

```bash
!split -b 200m allfiles.tar.gz allfiles.tar.gz.part.
```

This will split the archive into 200Mb blocks that you can download without a problem (if there is still a problem reduce the size by changing 200m to a lower value)

2. Then when you have downloaded all the split files reunite them on your system using the following command line (in a linux environment, or use cmder if you are on Windows):

```bash
cat allfiles.tar.gz.part.* > allfiles.tar.gz
```

## Reference

https://www.reddit.com/r/learnmachinelearning/comments/7er5ps/coursera_downloading_all_the_assignments_jupyter/
