#Playlist

#This program allows the user to create a play list of his favorite artists
#and songs.

def main():

    print("""
    Welcome to TuneList.
    Please input your favorite artists, and songs.
    We will create a playlist for you to look at.

    Press 1 to add an artist.
    Press 2 to delete an artist.
    Press 3 to view your playlist.
    Press 0 to exit the program.
    
""")
    
    playlist = {}
    song = []
    user_option = int(input("What would you like to do? "))

    while user_option != 0:
        if user_option == 1:
            user_artist = input("Please input an artist that you like. ")
            song = input("Please input your favorite song by that artist. ")
            playlist[user_artist] = song

            other_song = input("Would you like to add another song? ").lower

            if other_song == 'y':
                song = input("Please input your favorite song by that artist. ")
                playlist[user_artist] += song

            else:
                print("No other song was added. ")
                
        elif user_option == 2:
            del_artist = input("Please select an artist to delete. ")
            del(playlist[user_artist])
            
        elif user_option == 3:
            for music in playlist:
                print()
                print("Artist: ", music)
                print("Song: ", playlist[music])
                print()
                
        elif user_option == 0:
            print("The program is now closed")
            pass
        
        print()        
        user_option = int(input("What would you like to do? "))
        

            
    
main()
