# Coupon

Create new coupon:
```php
App\Coupon::create([
    'name' => "Valentine's Day",
    'discount' => '10',
    'type' => 1, // type: 1 = percantage , 2 = fixed
    'data' => 'custom_data',
]);
```

Assign coupon to user:
```php
$coupon = App\Coupon::find(1);
$user->coupon->set($coupon);
```

Remove assigned coupon:
```php
$coupon = App\Coupon::find(1);
$user->coupon->remove($coupon);
```

Remove all assigned coupons:
```php
$user->coupon->flush();
```

Apply or use all coupons:
```php
$user->coupon->apply();
or
$user->coupon->use();
```

Access all coupons that a user has used:
```php
$user->coupons;
```
