<p >
<a href="https://www.buymeacoffee.com/abhayrawat" target="_blank"><img align="center" src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" height="30px" width= "108px"></a>
</p> 

# simple_polls

simple_polls widget is polling widget with language localizations.

Liked my work ? [support me](https://www.buymeacoffee.com/abhayrawat)

## Example
for full example please view example/main.dart
```dart
SimplePollsWidget(
          onSelection: (PollFrameModel model, PollOptions selectedOptionModel) {
            print('Now total polls are : ' + model.totalPolls.toString());
            print('Selected option has label : ' + selectedOptionModel.label);
          },
          onReset: (PollFrameModel model) {
            print(
                'Poll has been reset, this happens only in case of editable polls');
          },
          optionsBorderShape: StadiumBorder(), //Its Default so its not necessary to write this line
          model: PollFrameModel(
            title: Container(
              alignment: Alignment.centerLeft,
              child: Text(
                'This is the title of poll. This is the title of poll. This is the title of poll.',
                style: TextStyle(
                  fontSize: 14,
                  fontWeight: FontWeight.w500,
                ),
              ),
            ),
            totalPolls: 100,
            endTime: DateTime.now().toUtc().add(Duration(days: 10)),
            hasVoted: false,
            editablePoll: true,
            options: <PollOptions>[
              PollOptions(
                label: "Option 1",
                pollsCount: 40,
                isSelected: false,
                id: 1,
              ),
              PollOptions(
                label: "Option 2",
                pollsCount: 25,
                isSelected: false,
                id: 2,
              ),
              PollOptions(
                label: "Option 3",
                pollsCount: 35,
                isSelected: false,
                id: 3,
              ),
            ],
          ),
        )
```
## Screenshots

![](https://raw.githubusercontent.com/abhay-s-rawat/simple_poll/main/images/en_options.jpg) ![](https://raw.githubusercontent.com/abhay-s-rawat/simple_poll/main/images/en_results.jpg) ![](https://raw.githubusercontent.com/abhay-s-rawat/simple_poll/main/images/it_options.jpg) ![](https://raw.githubusercontent.com/abhay-s-rawat/simple_poll/main/images/it_results.jpg)

>NOTE:
>Allowed language codes are it,fr,es,gr,en where en is default.
>This widget does not translate title and options, they should be translated by user.