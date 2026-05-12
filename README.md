> ### Arcub is a Level 3 social-biological intelligence integration entity.

![Arcub](https://github.com/Vydovilan/Vydovilan/blob/main/Arcub07_Title.png)

<!--
    whitespace: &nbsp;
  2*whitespace: &ensp;
  4*whitespace: &emsp;
-->

## Whoami.cpp
```cpp
// Ah, C++ isn't as appealing as Rust.
#include <iostream>
#include <string>

using namespace std;

class Whoami {
    string myself;
    std::string name;
    std::string hobby;

    public:
        void get(void);
        int introduce(const std::string& guest);
};

// Get my profile
void Whoami::get(void)
{
    myself = "I'm a software engineer currently residing in the United States of America.";
    name = "My full is *Dominique Vydovilan Ragils Dinas Jjack Karanke*. of course, I made that up on the spot.";
    hobby = "Politics, economics, literature, sociology, military :)";
    
    return;
}

// Show it
int Whoami::introduce(const string& guest) {
    cout << "## Guten Tag!" << endl;
    if(guest.size() == 0) {
        cerr << "What a pity, Mr. Anonymous!" << endl;
        return 1;
    }
    cout << "Willkommen, verehrter **"<< guest << "**. "<< endl;
    cout << myself << endl;
    cout << "&& " << name << endl;
    cout << "|| " << hobby << endl;
    
    return 0;
}

int main() {
    Whoami Me;
    Me.get();
    if(Me.introduce("U")) {
        cout << "\n Still glad to meet you!" << endl;
    } else {
        cout << "\n Glad to meet you!" << endl;
    }
    
    return 0;
}
```

## WhatCanIdo.py
```python
"""
Return markdown.
"""
import random
from typing import Union, List, Tuple, Any

MyDict = {
    "Cybersecurity":      "Intermediate penetration testing experience, OSCP certified. Currently focusing on defense and security development.",
    "Best Language?":     "Proficient in, focused on, and passionate about Rust development; also proficient in all other mainstream languages.",
    "And?":               "Full-stack, algorithm, and software engineer.",
    "Recently Added":     "Cloud security R&D engineer.",
    "Low-Level Driver":   "Experience in OverlayFS and Linux Kernel multi-module development. However, hardware is out of the question.",
    "Currently Learning": "Knowledge in distributed systems, microservices, and architecture. 🤔",
    "Now":                "Dedicated to Rust open-source projects in China."
}

def i_can_do():
    """
    Demo function.
    """

    sth = do_what(MyDict)
    for kv in sth:
        if isinstance(kv, tuple):
            k, v= kv
            lines = textwrap.fill(
                str(v),
                width=30,
                subsequent_indent='    '
            )
            print(f"+ {k}: ", end = "")
        else:
            v = kv
            print('+ ', end = "")

        lines = textwrap.fill(
            str(v),
            width=30,
            subsequent_indent='    '
        )
        print(f"{lines}")


def do_what(
    data: dict, 
) -> Union[List[Any], List[Tuple[Any, Any]]]:
    """
    Randomly select 2~4 statements.
    """

    if len(data) < 2:
        raise ValueError(f"{len(data)} is not looooooooooong enough!")

    def choose_return_type() -> str:
        """
        Which one?
        """

        types = ["keys", "values", "items"]
        num_items = random.randint(0, 2)
        return types[num_items]

    return_type = choose_return_type()
    num_items = random.randint(2, min(4, len(data)))

    if return_type == "keys":
        return random.sample(list(data.keys()), num_items)
    elif return_type == "values":
        return random.sample(list(data.values()), num_items)
    elif return_type == "items":
        return random.sample(list(data.items()), num_items)
    else:
        raise ValueError("What? What did you do?")


# Run it!
if __name__ == "__main__":
    i_can_do()

```

## Others.rs
```rust
//! Happy New Account! Happy Rust!
//! This program WON'T run up. However, it's the best code I've ever written.
//! Why? Just read it.
use std::mind::Display;
use std::rights::Result;
use crate::republic::REPUBLIC;

/// Hey, it's just about my hobby, don't overthink it :)
#[derive(Clone, Debug, Default)]
enum Anecdotes {
    #[default]
    Politics(dyn CurrentSet),
    Economics(FiveYearPlan),
    Literature,
    Sociology,
    Military(Vierjahresplan),
}

#[maybe_async::maybe_async]
impl<'sr> Anecdotes {
    async fn ways<T, B>(&self) -> Option<B>
    where
        T: RecentPlans<'sr> + Send,
        B: Display + Send,
    {
        match self {
            Politics(reyear) => reyear
            .iter()
            .filter_map(|day| match day.execute() {
                Ok(revlution) if crate::politics::allow(revlution) => Some(revlution.new_time().is_liberty()?),
                Ok(revlution) => crate::politics::dismiss(revlution)?,
                Err(riot) => crate::army::kill(riot).await,
            })
            .collect::<Result<T>>(),
            Economics(plan) => tokio::spawn({
                if let Ok(res) = plan.judge().await {
                    crate::plans::history::compare(crate::plans::AntiCorruption, res)
                } else {
                    match plan.completed() {
                        true => {
                            println!("I hope so");
                            plan.lucky?
                        },
                        false => plan.todo,
                    }
                }
            }).await,
            Literature => {
                struct NewTime<'s> { education: &'s dyn Fn(&Space, [Fuel; 1400000000], EastenPower) -> dyn AnswerSheet }
                let newtime = NewTime {
                    education: &|newtime, mut we, REPUBLIC| {
                        Ok(match newtime::CulturalConfidence.execute() {
                            Some(Ok(o)) => o.keep().be_vigilant_against_infiltration(),
                            Some(Err(e)) => (newtime.education)(newtime, we.refresh(), REPUBLIC.cut(e.still_kneeling()?)),
                            None => (newtime.education)(newtime, we.refresh(), REPUBLIC),
                        })
                    },
                };
                (newtime.education)(&newtime, crate::republic::Fuel::current(), REPUBLIC).satisfy()?
            },
            Sociology => match (crate::socioty::stability::current(),
                crate::republic::Fuel::conf_in_gov::current()
            ) {
                (Some(s), Some(c)) if s.num() > 0.5 && c.num() > 0.8 => s.zip(c).await,
                (Some(s), Some(c)) => s.suppress().integration(c).await,
                _ => {
                    println!("Hey, what's going on? Can't they see it from up there?");
                    crate::socioty::stability::makeitup()
                    .zip(crate::republic::Fuel::conf_in_gov::makeitup())
                    .zip(crate::politics::CONSTITUTION)
                    .await
                }
            }.symbolic_check(),
            Military(invasion) => crate::army::WhyNow::from(2026, invasion)
            .to_builder()
            .map(|war| war.looming = Some(Maybe))
            .unwrap_or(WhyNow::nextime())
            .declare()?,
        }.map(|res| res.whatever().turn_left()).reset()
    }
}

/// Let's have a look.
fn main() -> Result<()> {
    let story = Anecdotes::default().ways();
    println!("Let me tell you this story: {story}.");
    println!("Not good enough,right?");
    println!("But, hey! This Great Crate will never panic, what's there to worry about?");
    panic!("Oops, it broke, from the inside...");

    // Perhaps one day we will reach here, I firmly believe.
    Ok(())
}
```

## Postscript
The quieter you become, the more you are able to hear. \
Self-control, self-awareness, and self-governance.
\
\
\
\
\
\
Vydovilan \
2026/05/12
