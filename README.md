# Description

This user story lets a Line user to get today's schedules for every
movies at [CGV Blitz](https://www.cgv.id/en/schedule/cinema/0200).

# Web Scraping

- Using JSoup Library 


# Input Specs

- `/cgv_gold_class`
    - Retrieves all movies schedules that screened in Gold Class theatre
- `/cgv_regular_2d`
    - Retrieves all movies schedules that screened in Regular 2D theatre
- `/cgv_4dx_3d_cinema`
    - Retrieves all movies schedules that screened in 4DX 3D theatre
- `/cgv_velvet`
    - Retrieves all movies schedules that screened in Velvet Class theatre
- `/cgv_sweet_box`
    - Retrieves all movies schedules that screened in Sweet Box theatre
- `/cgv_change_cinema URL`
    - **URL** is the URL to the page displaying schedules for a CGV cinema,
    e.g. [CGV Grand Indonesia](https://www.cgv.id/en/schedule/cinema/0200),
    [CGV Pacific Place](https://www.cgv.id/en/schedule/cinema/0300)
    - By default, the bot retrieves data from CGV Grand Indonesia

# Output Specs

- For every commands except `/cgv_change_cinema`
    - Tuples of movie and their screening time, e.g. 
    ```
    ('King Arthur: Legend of the Sword', [11:00, 16:24])
    ('A Silent Voice', [16:30, 20:30])
    ```
    - If the theatre class does not exist at current CGV Blitz cinema,
    display an error message
- `/cgv_change_cinema URL`
    - A success message if the **URL** pointing to a valid CGV Blitz cinema
    page
    - Otherwise, display an error message
- Ensure that you follow **[defensive programming](https://en.wikipedia.org/wiki/Defensive_programming)**
and please make the error messages as helpful as possible!

# Definition of Done

- [x] Created or worked a module specific for containing functionalities related to this user story
- [x] Provided error handling for boundary cases and other exceptional cases
- [x] Build passed (i.e. not failed)
- [x] Have tested the working build on Heroku instance
