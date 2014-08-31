Please find the below steps to compile and run the programs-

Q1. hadoop fs -rmr /user/hxr121830/output_mvtop10
	hadoop fs -rmr /user/hxr121830/output_mvtop10_int
	hadoop jar top10.jar TopMoviesMain /user/hxr121830/input_mvdata/ratings.dat /user/hxr121830/output_mvtop10
	hadoop fs -cat /user/hxr121830/output_mvtop10/part-r-00000

Q2. hadoop fs -rmr /user/hxr121830/output_mvcount
	hadoop jar cMovies.jar CountMoviesMain /user/hxr121830/input_mvdata/movies.dat /user/hxr121830/output_mvcount
	hadoop fs -cat /user/hxr121830/output_mvcount/part-r-00000

Q3. hadoop fs -rmr /user/hxr121830/output__mvselected
	hadoop jar sMovies.jar SelectedMoviesMain /user/hxr121830/input_mvdata/movies.dat /user/hxr121830/output__mvselected Horror Action Comedy
	hadoop fs -cat /user/hxr121830/output__mvselected/part-r-00000
	
Note-
For Q1 => top10.jar
For Q2 => cMovies.jar
For Q3 => sMovies.jar