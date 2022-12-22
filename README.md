# Android TextView Copy, Paste & Share Button


## Copy Text

```
ClipboardManager clipboardManager = (ClipboardManager) getSystemService(Context.CLIPBOARD_SERVICE);
ClipData clipData = ClipData.newPlainText("TextView", editText.getText().toString());
assert clipboardManager!= null;
clipboardManager.setPrimaryClip(clipData);

Toast.makeText(getApplicationContext(), "Text Copyed", Toast.LENGTH_SHORT).show();
```

## Paste Text

```
ClipboardManager clipboard = (ClipboardManager) getSystemService(Context.CLIPBOARD_SERVICE);
ClipData.Item item = clipboard.getPrimaryClip().getItemAt(0);
textView.setText(item.getText().toString());

Toast.makeText(getApplicationContext(), "Text Pasted", Toast.LENGTH_SHORT).show();
```

## Share Text

```
Intent shareIntent = new Intent();
shareIntent.setAction(Intent.ACTION_SEND);
shareIntent.putExtra(Intent.EXTRA_TEXT, editText.getText().toString());
shareIntent.setType("text/plain");
shareIntent = Intent.createChooser(shareIntent, "Share Via:");
startActivity(shareIntent);
```


#### Better Understand - Watch Video - 

_© All Right Reserved by Innovative Programmer ❤️_

