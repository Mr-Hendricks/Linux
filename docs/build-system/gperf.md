<package-info :package="package" showsbu2></package-info>

<script>
		new Vue({
		el: '#main',
		data: { package: {} },
		mounted: function () {
				this.getPackage('gperf');
		},
		methods: {
			getPackage: function(name) {
					getPackage(name)
					.then(response => this.package = response);
			},
		}
  })
</script>

## Настройка

```bash
./configure --prefix=/usr --docdir=/usr/share/doc/gperf
```

## Сборка

```bash
make
```

## Тестирование

```bash
make -j1 check
```

## Установка

```bash
make install
```