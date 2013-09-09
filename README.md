Herbert's Time Machine
=======

> “It's against reason,” said Filby. <br/>
> “What reason?” said the Time Traveller. <br/>
> ― H.G. Wells, The Time Machine

Time travelling made simple.

----

#### Dear Friend,
If I may, I wish to propose to you a notion, no, an idea!

The idea that although some process, procedure or code of your own design may well function as expected in the
here and now, that no guarantees can be made with certainty that the same will function as well tomorrow.

And furthermore, some aspect of the device so thoughtfully rendered by yourself may by it's very nature be sensitive
to the natural forces of time. What I'm saying, my dear friend, is that you may expect the product to be varied given
the variable of the time of it's execution.

Now, I ask you this question, although no answer will be necessary, I assure you. How does one ensure the quality and
stability of their creations if one of the most basic and unchangeable variables of the universe can alter it's very
behavior?

Friend, I have for you, a bonafide, verifiable solution to this very problem. What you see before you is a device by
which the constructions of your invention can be sent through time to execute their tasks and produce their results
only to safely return at your immediate command.

You seem skeptical, friend, and understandably so. You'll notice that you've received a small instruction guide along
with this letter. I ask only that you take a moment to browse it's contents, and discover that you yourself have
unwittingly become a master of time travel.

_Very Truly Yours,_

_Uncle @apiguy_

----


### Installation

    $pip install herbert

### Usage
There are a few common ways of using Herbert's Time Machine. Notably you'll likely choose to use a context manager,
decorators, or manual control.

#### Using a context manager:

    from datetime import datetime
    from herbert import time_machine

    with time_machine.travel_to('tomorrow'):
        print "It is now one day in the future."
        print datetime.now()

    print "It is now present day."

    with time_machine.travel_to('11-05-2015'):
        print "The year is now 2015."
        print datetime.now()

    print "Once again, we've returned to the present."

#### Using decorators:

    from datetime import datetime
    from herbert import time_machine

    @time_machine.travel_to('yesterday')
    def do_yesterday():
        print "It's one day in the past here."
        print datetime.now()

#### Manual control:

    from datetime import datetime
    from herbert import time_machine

    time_machine.travel_to('1895')

    print "A great book is printed this year."
    print datetime.now()

    time_machine.return()

### Functions
Herbert's Time Machine comes with more than a few interesting functions for controlling time in various ways.

#### Travelling through time:

    time_machine.travel_to('4-26-1979')
    time_machine.travel_to('3 days from now')
    time_machine.travel_to(datetime.now() + timedelta(days=1))

#### Stopping time:

    time_machine.stop_time()  # Stops time at the current time
    time_machine.stop_time('next saturday') # Travels to next Saturday, then stops time

#### Slowing and speeding up time:

    time_machine.accelerate(10)  # Time moves 10 times as fast as normal
    time_machine.decelerate(100)  # Time moves 100 times slower than normal





