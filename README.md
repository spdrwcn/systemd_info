# `mac_conditions`


Supported platforms: Any version of Windows that supports WMIC.
## Example

```yaml
use systemd_info;

fn main() {
    
    let serial_number = systemd_info::get_bios_serial_number().unwrap();
    let cpu_name = systemd_info::cpu_name().expect("Failed to get CPU name");
    let ramgb = systemd_info::ram_info().expect("Failed to get RAM name");
    let disk_info = systemd_info::get_disk_info().expect("Failed to get DISK name");
    let gpu_name = systemd_info::get_gpu_info().expect("Failed to get GPU name");
    println!("Serial Number: {}", serial_number);
    println!("CPU Name: {}", cpu_name);
    println!("RAM: {} GB", ramgb);
    println!("Disk: {}", disk_info);
    println!("GPU: {}", gpu_name);
}
```

## License

`mac_conditions` is licensed under both MIT and Apache 2.0
