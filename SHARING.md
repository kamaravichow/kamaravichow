Share Image + Text 

```
Uri imageUri = Uri.parse("android.resource://" + getPackageName()
        + "/drawable/" + "ic_launcher");
 Intent shareIntent = new Intent();
 shareIntent.setAction(Intent.ACTION_SEND);
 shareIntent.putExtra(Intent.EXTRA_TEXT, "Hello");
 shareIntent.putExtra(Intent.EXTRA_STREAM, imageUri);
 shareIntent.setType("image/jpeg");
 shareIntent.addFlags(Intent.FLAG_GRANT_READ_URI_PERMISSION);
 startActivity(Intent.createChooser(shareIntent, "send"));
```
