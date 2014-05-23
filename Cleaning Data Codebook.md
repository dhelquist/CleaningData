      		CODE BOOK FOR RUN ANALYSIS MEANS

Overview of transformations:  
In order to clean up the data and make it tidy, I had to modify the column names to meet industry standards for column names as well as making data calculations less problematic from unnecessary characters.  I removed all the parentheses "()" and hyphens "-", and made all the characters lowercase.  To separate key words or characters within my column names, I used the period "." to make it easier for the reader to read.

I reviewed each of the column names to ensure that their meanings were clear and distinct.  I made the decision explicitly to make little/no additional modifications to the column names beyond the above changes.

Below is a definition of each column name in my table with a description of what it represents:


COL#	NAME:	DESCRIPTION:

1	SubID
		Subscriber ID, unique to each subscriber

2	Activity
		The activity being done while the measurements were taking place.  Activities include the following:
			- Laying
			- Sitting
			- Standing
			- Walking
			- Walking Down Stairs
			- Walking Up Stairs

3	tbodyacc.mean.x
		Time signal - mean body acceleration in the 'x' direction

4	tbodyacc.mean.y
		Time signal - mean body acceleration in the 'y' direction

5	tbodyacc.mean.z
		Time signal - mean body acceleration in the 'z' direction

6	tbodyacc.std.x
		Time signal - standard deviation of the body's acceleration in the 'x' direction

7	tbodyacc.std.y
		Time signal - standard deviation of the body's acceleration in the 'y' direction

8	tbodyacc.std.z
		Time signal - standard deviation of the body's acceleration in the 'z' direction

9	tgravityacc.mean.x
		Time signal - mean gravity acceleration in the 'x' direction

10	tgravityacc.mean.y
		Time signal - mean gravity acceleration in the 'y' direction

11	tgravityacc.mean.z
		Time signal - mean gravity acceleration in the 'z' direction

12	tgravityacc.std.x
		Time signal - standard deviation of gravity acceleration in the 'x' direction

13	tgravityacc.std.y
		Time signal - standard deviation of gravity acceleration in the 'y' direction

14	tgravityacc.std.z
		Time signal - standard deviation of gravity acceleration in the 'z' direction

15	tbodyaccjerk.mean.x
		Time signal - mean body jerk acceleration in the 'x' direction

16	tbodyaccjerk.mean.y
		Time signal - mean body jerk acceleration in the 'y' direction

17	tbodyaccjerk.mean.z
		Time signal - mean body jerk acceleration in the 'z' direction

18	tbodyaccjerk.std.x
		Time signal - standard deviation of body jerk acceleration in the 'x' direction

19	tbodyaccjerk.std.y
		Time signal - standard deviation of body jerk acceleration in the 'y' direction

20	tbodyaccjerk.std.z
		Time signal - standard deviation of body jerk acceleration in the 'z' direction

21	tbodygyro.mean.x
		Time signal - mean body angular velocity in the 'x' direction

22	tbodygyro.mean.y
		Time signal - mean body angular velocity in the 'y' direction

23	tbodygyro.mean.z
		Time signal - mean body angular velocity in the 'z' direction

24	tbodygyro.std.x
		Time signal - standard deviation of body angular velocity in the 'x' direction

25	tbodygyro.std.y
		Time signal - standard deviation of body angular velocity in the 'y' direction

26	tbodygyro.std.z
		Time signal - standard deviation of body angular velocity in the 'z' direction

27	tbodygyrojerk.mean.x
		Time signal - mean of the body's angular velocity of jerks in the 'x' direction

28	tbodygyrojerk.mean.y
		Time signal - mean of the body's angular velocity of jerks in the 'y' direction

29	tbodygyrojerk.mean.z
		Time signal - mean of the body's angular velocity of jerks in the 'z' direction

30	tbodygyrojerk.std.x
		Time signal - standard deviation of the body's angular velocity of jerks in the 'x' direction

31	tbodygyrojerk.std.y
		Time signal - standard deviation of the body's angular velocity of jerks in the 'y' direction

32	tbodygyrojerk.std.z
		Time signal - standard deviation of the body's angular velocity of jerks in the 'z' direction

33	tbodyaccmag.mean
		Time signal - mean of the Euclidean magnitude of the body's acceleration

34	tbodyaccmag.std
		Time signal - standard deviation of the Euclidean magnitude of the body's acceleration

35	tgravityaccmag.mean
		Time signal - mean of the Euclidean magnitude of gravity's acceleration

36	tgravityaccmag.std
		Time signal - standard deviation of the Euclidean magnitude of gravity's acceleration

37	tbodyaccjerkmag.mean
		Time signal - mean of the Euclidean magnitude of the body's jerking acceleration

38	tbodyaccjerkmag.std
		Time signal - standard deviation of the Euclidean magnitude of the body's jerking acceleration

39	tbodygyromag.mean
		Time signal - mean of the Euclidean magnitude of the body's angular velocity

40	tbodygyromag.std
		Time signal - standard deviation of the Euclidean magnitude of the body's angular velocity

41	tbodygyrojerkmag.mean
		Time signal - mean of the Euclidean magnitude of the body's jerking angular velocity

42	tbodygyrojerkmag.std
		Time signal - standard deviation of the Euclidean magnitude of the body's jerking angular velocity

43	fbodyacc.mean.x
		Frequency Domain Signal - mean body acceleration in the 'x' direction

44	fbodyacc.mean.y
		Frequency Domain Signal - mean body acceleration in the 'y' direction

45	fbodyacc.mean.z
		Frequency Domain Signal - mean body acceleration in the 'z' direction

46	fbodyacc.std.x
		Frequency Domain Signal - standard deviation of the body's acceleration in the 'x' direction

47	fbodyacc.std.y
		Frequency Domain Signal - standard deviation of the body's acceleration in the 'y' direction

48	fbodyacc.std.z
		Frequency Domain Signal - standard deviation of the body's acceleration in the 'z' direction

49	fbodyacc.meanfreq.x
		Frequency Domain Signal - mean frequency of body acceleration in the 'x' direction

50	fbodyacc.meanfreq.y
		Frequency Domain Signal - mean frequency of body acceleration in the 'y' direction

51	fbodyacc.meanfreq.z
		Frequency Domain Signal - mean frequency of body acceleration in the 'z' direction

52	fbodyaccjerk.mean.x
		Frequency Domain Signal - mean of body's jerk acceleration in the 'x' direction

53	fbodyaccjerk.mean.y
		Frequency Domain Signal - mean of body's jerk acceleration in the 'y' direction

54	fbodyaccjerk.mean.z
		Frequency Domain Signal - mean of body's jerk acceleration in the 'z' direction

55	fbodyaccjerk.std.x
		Frequency Domain Signal - standard deviation of body's jerk acceleration in the 'x' direction

56	fbodyaccjerk.std.y
		Frequency Domain Signal - standard deviation of body's jerk acceleration in the 'y' direction

57	fbodyaccjerk.std.z
		Frequency Domain Signal - standard deviation of body's jerk acceleration in the 'z' direction

58	fbodyaccjerk.meanfreq.x
		Frequency Domain Signal - mean frequency of body's jerk acceleration in the 'x' direction

59	fbodyaccjerk.meanfreq.y
		Frequency Domain Signal - mean frequency of body's jerk acceleration in the 'y' direction

60	fbodyaccjerk.meanfreq.z
		Frequency Domain Signal - mean frequency of body's jerk acceleration in the 'z' direction

61	fbodygyro.mean.x
		Frequency Domain Signal - mean body angular velocity in the 'x' direction

62	fbodygyro.mean.y
		Frequency Domain Signal - mean body angular velocity in the 'y' direction

63	fbodygyro.mean.z
		Frequency Domain Signal - mean body angular velocity in the 'z' direction

64	fbodygyro.std.x
		Frequency Domain Signal - Standard deviation of body angular velocity in the 'x' direction

65	fbodygyro.std.y
		Frequency Domain Signal - Standard deviation of body angular velocity in the 'x' direction

66	fbodygyro.std.z
		Frequency Domain Signal - Standard deviation of body angular velocity in the 'x' direction

67	fbodygyro.meanfreq.x
		Frequency Domain Signal - mean frequency body angular velocity in the 'x' direction

68	fbodygyro.meanfreq.y
		Frequency Domain Signal - mean frequency body angular velocity in the 'y' direction

69	fbodygyro.meanfreq.z
		Frequency Domain Signal - mean frequency body angular velocity in the 'z' direction

70	fbodyaccmag.mean
		Frequency Domain Signal - mean of the Euclidean magnitude of the body's acceleration

71	fbodyaccmag.std
		Frequency Domain Signal - standard deviation of the Euclidean magnitude of the body's acceleration

72	fbodyaccmag.meanfreq
		Frequency Domain Signal - mean frequency of the Euclidean magnitude of the body's acceleration

73	anglex.gravitymean
		Frequency Domain Signal - mean of gravities angular acceleration in the 'x' direction

74	angley.gravitymean
		Frequency Domain Signal - mean of gravities angular acceleration in the 'y' direction

75	anglez.gravitymean
		Frequency Domain Signal - mean of gravities angular acceleration in the 'z' direction