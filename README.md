
# Left Join

- Movies Table

movies = pd.read_csv("tmdb_movies.csv")
print(movies.head())
print(movies.shape)


      id      original_title        popularity      release_date
0     257     20.415572             20.415572       2005-09-23
1     14290   3.877036              3.877036        2002-01-12
2     38365   38.864027             38.864027       2010-06-24
3     9672    3.680895              3.680895        2006-11-16
4     12819   12.300789             12.300789       2010-09-17

(4803,4)

- Tagline Table

taglines = pd.read_csv("tmdb_taglines.csv")
print(taglines.head())
print(taglines.shape)

      id          tagline
0     19995       Enter the World of Pandora
1     285         At the end of the world, the adventures begins
2     206647      A Plan No One Escapes
3     49026       The Legends Ends
4     49529       Lost in our world, found in another

(3955, 2)


- Merge with Left Join

movies_taglines = movies.merge(taglines, on="id", how="left")
print(movies_taglines.head())

      id      original_title        popularity      release_date    tagline
0     257     20.415572             20.415572       2005-09-23      NaN
1     14290   3.877036              3.877036        2002-01-12      Never undere
2     38365   38.864027             38.864027       2010-06-24      Boys will be
3     9672    3.680895              3.680895        2006-11-16      There's more
4     12819   12.300789             12.300789       2010-09-17      A Pawsome 3D

- Number of rows returned

prinr(movies_taglines.shape)

(4803, 5)



